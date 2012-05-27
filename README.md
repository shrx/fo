fo
==
fo, short for Find & Open, is a ksh script that finds all folders with a given name and, if a single folder is found, opens it.

Prerequisites, dependencies
---------------------------
You need to have [ksh][1] installed. The script doesn't work in bash because changes to variables are lost within a piped process. You can read a discussion about this [here][2].

[1]: http://www.kornshell.com/
[2]: http://ubuntuforums.org/showthread.php?t=312017

Usage
-----
Run the script when you want to find and open a chosen folder, for example: `fo foo bar` will search for folders named "foo bar" (case insensitive).
If a single folder is found, it will open.
If more folders are found, their locations will be displayed instead. You may then enter the desired location's index number and that location will open.
The script uses the `locate` command so recently created folders might not yet be in the database. I chose `locate` over `find` because it's much faster.