# GameMaker's dev guide for learning Bento

This a guide for practical use of Bento from a GameMaker dev perspective. 

## Getting Started

Install the following programs to get started:

* *NodeJS*: enables command line scripts/tools for Bento
	* After installation, open *Cmd* (on Windows) or *Terminal* (on Mac) and type:
	* npm install -g jshint
	* npm install -g gulp
	* npm install -g gulp-cli
	* npm install -g cordova@9.0.0
	* npm install -g bento-game-engine
	* (Use sudo for Mac)
* *MAMP*: web server
* *Chrome*: browser
* *Sublime Text 3*: text editor (any other text editor is fine, but we made useful plugins for ST3)
* Git (any client of choice), recommended: SourceTree or Fork

## Knowledge required

Not required but extremely helpful:

* JavaScript
* Working with command line interfaces -> using Cmd on Windows and Terminal on Mac
* NodeJS environment and npm
* RequireJS
* Git

## Running and developing a Bento game

Download an empty template project using the bento-game-engine npm package. If NodeJS is installed correctly and you installed the package using `npm install -g bento-game-engine`, you will be able to use `bento` command in Cmd (on Windows). This enables you to download a template project in your current working directory. 

Bento games are actually HTML pages. As such, you typically use a browser to run a Bento game. The main starting point is index.html, but opening that file won't run the game yet (not in Chrome at least, more on Chrome later). It requires a web server that can handle http requests. MAMP is an easy to use web server. After opening MAMP, set the main directory to your project directory and navigate your browser to `http://localhost:8080` (where 8080 is the port number). This will automatically open the index.html in the main directory if it exists.

Chrome is not required, you can use any browsers. In any case, always keep the JavaScipt console open (ctrl+shift+j on Windows). Highly recommended to turn off the cache (find the ... button and enable the Network Conditions tab, in there check the Disable Cache option). Also turn on the mobile emulator (ctrl+shift+m on Windows), this will emulate the sizes and orientations of mobile phones.

There are several tools/scripts written for NodeJS to help with development. Type `gulp` in the Cmd to see the default options.

Starting point for developemnt is the file `js/screens/main.js`

## Working with Sublime Text 3

Sublime Text is technically not free software, though there is a unlimited trial (it will nag you with a popup). Recommended to drag your project folder from Explorer/Finder to the ST3 window to get the project view.

Sublime Text 3 is most powerful when also using the plugins, or packages as ST3 calls them. Recommended are the following:

* Follow instructions on https://packagecontrol.io, press `ctrl+shift+p`, type in `Install package` and install:
* JSHint: plugin that can check syntax errors
* Sublime Linter: base plugin that checks syntax errors realtime
* Sublime Linter - JSHint: plugin for jshint
* Build on save: will run JSHint after saving a file
* A file icon: default icons on Sublime Text 3 look really ugly
* Bento AMD --> manual installation https://github.com/LuckyKat/bento-amd-tool 
  Sublime Packages folder at Preferences->Browse packages
* Fold JS Functions: Makes folding code in ST3 easier


## Basic JavaScript knowledge

Javascript's syntax is very similar to GML. However keep some main differences in mind.

* Always use `var` to declare variables. Where GML uses this to declare local variables, in JavaScript if you miss it, you are declaring a global variable.
* Scope in GML is usually restricted to the script file, in JavaScript
* Using data structures are much easier (particularly object literals are very useful, comparible to maps)
* In JavaScript, using `with` is considered bad practice

More details can be read in this short guide for JavaScript here https://www.lucky-kat.com/javascript

## Bento vs GameMaker

* Bento does not have a visual editor (yet). 
* Default settings in a Bento empty project is to run a game in 60 fps without delta time.
* *Screens* in Bento are the equivalent of *rooms* in GM 
* Objects/instances are called entities. Entities get behavior by attaching components. Components are objects with functions --> the `update` function is the equivalent of the step function. (see Bento guide for more details)
* Sprites are components (see Bento guide for more details)

## Further reading

* Bento guide (slightly incomplete and outdated): https://github.com/LuckyKat/Bento/blob/master/guide.md
* Bento documentation: https://luckykat.github.io/Bento/
* JavaScript guide: https://www.lucky-kat.com/javascript
