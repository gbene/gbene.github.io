+++
date = '{{ .Date }}'
title = '{{ replace .File.ContentBaseName "-" " " | title }}'
tags = ["library"]
description = ""
showdate = true
showtags = false
firstauthor=true
contributingauthor=false
repo=""
docs=""
+++
![logo](/'{{ replace .File.ContentBaseName "-" " " | title }}'/logo.png)
