List LESS variables
======================

Simple Sublime 2/3 plugin for listing LESS variables used in a file.

The default hotkey is <kbd>Ctrl</kbd>+<kbd>Alt</kbd>+<kbd>L</kbd> (or <kbd>Ctrl</kbd>+<kbd>Shift</kbd>
+<kbd>L</kbd> on Linux to avoid conflicts with the lock screen hotkey).

It displays a list of LESS variables used in your current file allowing you to insert a selected one 
directly into your code. It also supports `@import`ed LESS files so you can use variables defined in 
external files.

Note that the plugin automatically ignores anything which looks like a vendor prefixed statement (e.g. 
`@-webkit-keyframes`) and reserved words (e.g. `@media`, `@import` etc.)

![Screenshot](http://i41.tinypic.com/eajivq.png)

Please note that the plugin currently does not understand variable scope and therefore will display all 
the occurances of a variable.

Installation
------------
You can use the Sublime Package Manager to install this plugin.