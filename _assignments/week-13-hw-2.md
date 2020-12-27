---
title: Simple Text Editor
week: 13
homework: 2
---

The skeleton of a simple text editor is provided using JavaFX.  Recall the various file interaction methods from week 4.
Implement the button handlers for the following toolbar actions:

* New- creates a new blank file
* Open - opens a file browser to select a file and loads the selected file into the editor pane
* Save As - opens a file browser and saves the current content of the editor pane to the new file in the location chosen in the browser
* Save - replaces the contents of the currently open file with the contents of the editor.  This option should be disabled for a new file that has not yet been saved using Save As

JavaFX provides a built-in file chooser that you should use.  You can read the documentation for it here: https://docs.oracle.com/javase/8/javafx/api/javafx/stage/FileChooser.html
