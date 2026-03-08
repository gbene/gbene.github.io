+++
date = '2022-02-22'
draft = false
title = 'Tslist converter'
tags = ["project"]
description = "online WRF tslist to csv converter"
showdate = true
showtags = false
link=""
+++


TS lists are a type of output files that are produced by WRF during a simulation to register the calculated values in specific coordinates. The raw output format of these files is not universal and it makes importing this kind of data a big hassle in other programs (such as excel). To contrast this problem I created this page that can be used to convert any TSLISTS in a properly formatted csv file and if necessary do some simple conversion and calculations (such as converting the time column from hours to days).

This converter uses javascript to import and manipulate the data. Everything is done locally so it works even offline if the page is saved.

Here is a [sample file](/tslist/jct.d01_CONUS.TS) to test the converter 

<hr>

<!DOCTYPE html>
<html>
<head>
  <meta charset="UTF-8">
  <title>File(s) size</title>
  <style>
    html {
        font-family: sans-serif;
    }
    div#drop_box {
          height: 400px;
          width: 400px;
          border: 3px solid;
          display: flex;
          justify-content: center;
          flex-direction: column;
          align-items: center;
          border-radius: 4px;
      }
      input[type='file'] {
  color: transparent;
}
      button, input[type='file']::file-selector-button {
        background-color: #4CAF50; /* Green */
        border: none;
        color: white;
        padding: 10px 15px;
        text-align: center;
        text-decoration: none;
        display: inline-block;
        font-size: 20px;
        border-radius: 3px;
      }
      pre {
        display: -webkit-box;
        -webkit-line-clamp: 10;
        -webkit-box-orient: vertical;
      }
      .dropBox{
        font-size: 1.15em;
      }
      .formCtrl{
          font-size: 1.15em;
          font-weight: normal;
          line-height: 1.1;
          display: grid;
          grid-template-columns: 1em auto;
          gap: 0.5em;
      }
      input[type='radio']{
        width: 1em;
        height: 1em;
      }
    </style>
</head>
  <h2>Input</h2>
    <input type="file" id="file-selector"  multiple>
   <br>
    or
      <div id="drop_box">
        <label class="dropBox">Drop here</label>
      </div>
      <!-- <h5>Chosen file/s</h5> -->
      <pre id='fileBox'>Chosen file/s </pre>
      <h2>Conversion options</h2>
      Converted values are appended as a last column
      <label for="convertTimeDay" class="formCtrl">
        <input type="radio" id="convertTimeDay" value="td" name='timeopt'>
        Convert hours in days
      </label>
      <label for="convertTimeMin" class="formCtrl">
        <input type="radio" id="convertTimeMin" value="tm" name='timeopt'>
        Convert hours in minutes
      </label>
      <label for="convertTimeSec" class= "formCtrl">
        <input type="radio" id="convertTimeSec" value="ts" name='timeopt'>
         Convert hours in seconds
       </label>
       <label for="convertNone" class= "formCtrl">
         <input type="radio" id="convertNone" value="ts" name='timeopt' checked="checked">
          Leave as is
        </label>
       <br>
      <button type="button" id="convert_button"><i class="fas fa-exchange-alt"></i> Convert!</button>
      <hr>
      <h2>Output</h2>
      <pre id='output'> </pre>
      <button type="button" id="save_button" onclick="saveCSV()"><i class="fa fa-save"></i> Save</button>
      <script>
        function displayOutput(text){
          const outBox = document.getElementById('output');
          outBox.textContent = '';
          outBox.textContent = text;
        }
        function saveCSV(){
          // console.log(newCSV)
          const  blob = new Blob([newCSV], {type: 'text/plain'});
          const inFileName = fileList[0].name
          const fileName = inFileName + '_toCSV.csv';
          let newLink = document.createElement('a');
          newLink.download = fileName;
          newLink.href = window.webkitURL.createObjectURL(blob);
          // newLink.style.display = 'none';
          // document.body.appendChild(newLink);
          newLink.click();
        }
        const tdCheckBox = document.getElementById('convertTimeDay');
        const tmCheckBox = document.getElementById('convertTimeMin');
        const tsCheckBox = document.getElementById('convertTimeSec');
        const fileSelector = document.getElementById('file-selector');
        const fileNameBox = document.getElementById('fileBox');
        fileSelector.addEventListener('change', (event) => {
          window.fileList = event.target.files;
          fileNameBox.textContent = event.target.files[0].name
        });
        const convertButton = document.getElementById('convert_button')
        convertButton.addEventListener('click',(event)=>{
          var reader = new FileReader();
          var header = 'id;ts_hour;id_tsloc;ix;iy;t;q;u;v;psfc;glw;gsw;hfx;lh;tsk;tslb(1);rainc;rainnc;clw\n';
          reader.onload = function(){
              var infileName = window.fileList[0].name;
              var text = reader.result;
              var csv = header+text.split('\n').slice(1).join('\n').replace(/ \s+/g,';');
              // CSV and data manipulation
              var lines = csv.split('\n');
              var result = [];
              var headers = lines[0].split(';');
              for(var i=1; i<lines.length;i++){
                var obj = {};
                var currentline = lines[i].split(';');
                // console.log(currentline)
                for(var j=0;j<headers.length;j++){
                  obj[headers[j]] = currentline[j];
                }
                result.push(obj);
              }
              var jString = JSON.stringify(result);
              var jDF = JSON.parse(jString);
              // console.log(Object.values(jDF[0]));
              // DO stuff here
              for (i=0;i<jDF.length;i++){
                if (tdCheckBox.checked == true){
                  jDF[i]['ts_days'] = jDF[i]['ts_hour']/24;
                }
                else if (tmCheckBox.checked == true){
                  jDF[i]['ts_minutes'] = jDF[i]['ts_hour']*60;
                }
                else if (tsCheckBox.checked == true){
                  jDF[i]['ts_seconds'] = jDF[i]['ts_hour']*3600;
                }
              }
              // for(var k=0;j< jDF.length;k++){
              //   console.log(jDF[k]);
              // }
              // console.log(jDF.length);
              // Save stuff
              // var keys = Object.keys(jDF[0]);
              window.newCSV = Object.keys(jDF[0]).join(';').trim()+'\n';
              for (i=0;i<jDF.length;i++){
                var line = Object.values(jDF[i]).join(';').trim()+'\n';
                newCSV = newCSV+line
              }
              displayOutput(newCSV)
            }
            var files = window.fileList;
            reader.readAsText(files[0]);
          // console.log(reader.readAsDataURL(window.fileList[0]));
        });
        const dropZone = document.getElementById('drop_box');
        dropZone.addEventListener('dragover',(event)=>{
          event.stopPropagation();
          event.preventDefault();
          // Style the drag-and-drop as a "copy file" operation.
          event.target.style.border = "4px solid teal";
          event.target.style.color = "teal";
          event.target.style.fontWeight = "bold";
          event.dataTransfer.dropEffect = 'copy';
        });
        dropZone.addEventListener('dragleave',(event)=>{
          event.stopPropagation();
          event.preventDefault();
          // Style the drag-and-drop as a "copy file" operation.
          event.target.style.border = "3px solid";
          event.target.style.color = "";
          event.target.style.fontWeight = "normal";
        });
        dropZone.addEventListener('drop', (event) => {
          event.stopPropagation();
          event.preventDefault();
          event.target.style.border = "3px solid";
          event.target.style.fontWeight = "normal";
          event.target.style.color = "";
          window.fileList = event.dataTransfer.files;
          fileNameBox.textContent = fileList[0].name
        });
      </script>
</html>

