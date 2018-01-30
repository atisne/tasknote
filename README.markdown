tasknote
========

The script automatically opens your text editor (defaults to vim) and allows you to edit notes. Upon saving notes, an annotation is added to the task to alert you to the fact that notes exist for that task. The annotation captures the first line of the note file and is updated with every modification to the file.

History
-------
* Original implementation: Alan Bowen
* Update to taskwarrior 2.0: Michael Bobroski
* Context-aware annotations: Bjoern Doebel

Usage
-----

**Create/Edit Note:**

`tasknote <task_id>`

**View Note:**
	
`tasknote <task_id> v`

**Delete Note:**
	
`tasknote <task_id> d`

Configuration
-------------
Save in a place like /usr/bin and flag as executable with sudo chmod a+x /usr/bin/tasknote.

You can adjust the FOLDER variable (tasknotes location) in the script. If the path does not exist, you will be asked if you want to create it during the first run.

You can also configure the EDITOR (default: vim), VIEWER (default: cat), as well as NOTEMSG, the annotation message appended to the task in taskwarrior.

Todo
----
Add a Purge action to purge notes with no associated task (purged tasks, version 2.6.0 of taskwarrior)
