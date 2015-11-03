# Base Project for Harp.js
[Harp.js](http://harpjs.com) is a static site generator built on top of node.js.

## Markup and code
HTML is written in [Jade](http://jade-lang.com).
CSS is written in [Stylus](https://learnboost.github.io/stylus/).
Javascript is written in [Coffeescript](http://coffeescript.org).

## Naming
* File names are separated with an _ (file_name).
* CSS names are separated with - (class-name)
* Javascript variables are separated with camel case (variableName)

## Project structure
Everything inside the root folder above the project root are required files for harp.js, with the exception of a .gitignore file.

**To do**: Go ahead and create a .gitignore files, and paste in the following text, which will ignore hidden OS X files and the files node needs to run, which we’ll get separately:
.DS_store
node_modules

Main project files belong in **/public**, which is the “project root”.

There are three key files inside the project root, based on harp.js conventions:
1. **index.jade**: the home page of the site, which includes code that belongs in the body of the home page.
2. **_layout.jade**: the shared main layout file of the site, which includes a shared **head** and **body**.
3. **404.jade**: the markup for the 404 page.

There are four core folders inside the project root:
1. **/components**
2. **/stylesheets**
3. **/images**
4. **/fonts**

### /components
Pages are built from components which each have their own .jade file. For example; header.jade or who_we_are.jade. There is a base header.jade and footer.jade included by default.

### /stylesheets
CSS files belong here. Keeping CSS separated into component files matching the component layout .jade files helps keep the code organized and searchable. At the root belong two files and two folders:
1. **main.styl**: This includes @import links to the rest of your stylesheets, and possibly a small amount of shared global CSS rules.
2. **reset.styl**: A standard CSS reset file, to standardize rules across browsers.
3. **/helpers**: A folder containing a set of base rules to be used across the site, including color variables (color.styl), font references (font.styl), typography rules (type.styl) and a flex-box based grid framework (lettuce-wrap.styl).
4. **/components**: Each component .jade file requires a matching .styl file.

### /images & /fonts
Contains image files and font files, respectively.

## Installing harp.js
Follow instructions [here](http://harpjs.com/docs/environment/install) to setup harp.js. If you already	

## Final steps
Replace this readme.md with relevant notes for the project.
