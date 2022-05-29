# **Practice in the Terminal**
## ***`Introduction`***
#### Unix likes to take the approach of giving you a set of building blocks and then letting you put them together. This allows us to build things to suit our needs. With a bit of creativity and logical thinking, mixed in with an appreciation of how the blocks work, we can assemble tools to do virtually anything we want.
## ***`The Command Line!`***
#### A command line, or terminal, is a text based interface to the system. You are able to enter commands by typing them on the keyboard and feedback will be given to you similarly as text.

#### The command line typically presents you with a prompt. As you type, it will be displayed after the prompt. Most of the time you will be issuing commands.

#### open a terminal in Windows and intend to remotely log into another machine then you will need an SSH client. A rather good one is Putty (free).
## ***`Basic Navigation!`***
#### - 'pwd' which stands for Print Working Directory,  It tells what the current or present working directory is.
#### - Absolute and Relative Paths, Whenever we refer to a file or directory we are using one of these paths. Whenever we refer to a file or directory, we can, in fact, use either type of path (either way, the system will still be directed to the same location).
#### ~ (tilde) - This is a shortcut for your home directory. eg, if your home directory is /home/ryan then you could refer to the directory Documents with the path /home/ryan/Documents or ~/Documents
#### . (dot) - This is a reference to your current directory. eg in the example above we referred to Documents on line 4 with a relative path. It could also be written as ./Documents (Normally this extra bit is not required but in later sections we will see where it comes in handy).
#### .. (dotdot)- This is a reference to the parent directory. You can use this several times in a path to keep going up the hierarchy. eg if you were in the path /home/ryan you could run the command ls ../../ and this would do a listing of the root directory.
#### cd (change directory),In order to move around in the system
#### ls, List the contents of a directory
## ***`More About Files!`***
#### This one can sometimes be hard to get your head around but as you work through the sections it will start to make more sense. A file extension is normally a set of 2 - 4 characters after a full stop at the end of a file, which denotes what type of file it is.
#### Other systems such as Windows are case insensitive when it comes to referring to files. Linux is not like this. As such it is possible to have two or more files and directories with the same name but letters of different case.
#### If we wanted to move into a directory with space between 2 words we must use quotes'' or escape characters\.
#### ls -a, List the contents of a directory, including hidden files.
## ***`Manual Pages!`***
#### The manual pages are a set of pages that explain every command available on your system including what they do, the specifics of how you run them and what command line arguments they accept. Some of them are a little hard to get your head around but they are fairly consistent in their structure so once you get the hang of it it's not too bad. You invoke the manual pages with the following command:

#### - man <command to look up
#### - man <command,Look up the manual page for a particular command.
#### - man -k <search term, Do a keyword search for all manual pages containing the given search term.
#### - /<term, Within a manual page, perform a search for 'term'
#### - n, After performing a search within a manual page, select the next found item.

## ***`File Manipulation!`***
#### mkdir, Make Directory - ie. Create a directory.
#### rmdir, Remove Directory - ie. Delete a directory.
#### touch, Create a blank file.
#### cp, Copy - ie. Copy a file or directory.
#### mv, Move - ie. Move a file or directory (can also be used to rename).
#### rm, Remove - ie. Delete a file.

## ***`Cheat Sheet `***
#### Cheat Sheet [here](https://ryanstutorials.net/linuxtutorial/cheatsheet.php)
