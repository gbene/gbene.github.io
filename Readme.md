Personal website repository. The repo is structured as follows:
1. `site-builder` branch containing all the hugo files to build and test the site
2. `gh-pages` branch containing the result of the huog build

Pages is set so that it points to `gh-pages` branch and there is a workflow that activates each time there is a push on `site-builder`.