## Pre Commit Hook For Sketch

Based on https://gitlab.com/gitlab-org/gitlab-design/tree/master


- Automatic Sketch previews based on a pre-commit hook
  - The pre-commit hook will auto generate preview images out of your Sketch pages 
  with sketchtool


- Semi automatic Sketch spec previews with Continuous Integration
  - Whenever you create a spec preview folder with the Sketch Measure Plugin, append 
  spec-previews to the name of the generated directory and it will be visible by an URL. Search in https://gitlab-org.gitlab.io/gitlab-design

- Automatic live Framer prototypes with Continuous Integration
  - Whenever you save a Framer prototype in this repository and commit push it to 
  GitLab, it will automatically be hosted in the same way as the spec previews superpower. See them live at https://gitlab-org.gitlab.io/gitlab-design

- Standalone Live Html Previews
  - *By using the wget command: wget -kN --html-extension URL or wget -E -p -k URL 
  you can create a standalone working HTML page of the GitLab view you want. Just change the name of the file to index.html and append html-previews to the name of the directory it will be inside of. Good luck! (No guarantees with this one!)


- Sketch Diffs
  - Add the following to your .git/config file to see if you are having merge 
  conflicts with a shared .sketch design file
    ```[diff "sketchtool"]
      textconv = "sketchtool dump"
      cachetextconv = true
      binary = true



### Activating them!
- Install Sketch
- Copy the pre-commit file into your .git/hooks/ folder
- The pre-commit hook will auto generate preview images out of your sketch pages
- Install [Sketch Toolbox](http://sketchtoolbox.com/)
- Install [Sketch Measure Plugin](https://github.com/utom/sketch-measure) with the Sketch Toolbox
