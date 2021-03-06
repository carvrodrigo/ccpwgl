CCP WebGL Library
======

This project now uses the glMatrix v2.4.0 library and is no longer compatible with the previously used version (0.9.x)


Building
------

Building ccpwgl requires [Node.js](http://www.nodejs.org) and [Grunt](http://www.gruntjs.com) installed.
After installing, run ```npm install``` once, which downloads the dependencies.

If you are on Windows you will also need to install the Grunt CLI globally with ```npm install -g grunt-cli```.

When all is set up, ```grunt [task]``` starts the build script.

The default task runs the tasks "cc", "format", "min". "lint" is currently not in the
chain for still reporting too many errors.

**Available tasks**:
* format: running jsbeautifier (based on .jsbeautifyrc)
* lint: running jshint (based on .jshintrc)
* min: running uglifyjs, producing `/dist/ccpwgl_int.min.js`
* cc: running concat and jsbeautifier:cc producing `/dist/ccpwgl_int.js`
* dist: running `min` and `cc` which compiles the ccpwgl_int files

Documentation (Work in progress)
--------------------------------
The following command line will create jsdoc html documentation in the `/docs` folder
* > `jsdoc -c .jsdocs -d docs` (Windows users will need to add jsdocs to their path variables)
