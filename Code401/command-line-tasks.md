# Bash Command Line Tutorials

<https://ryanstutorials.net/linuxtutorial/>

## The Command Line

<https://ryanstutorials.net/linuxtutorial/commandline.php>

Within a terminal you have what is known as a shell. This is a part of the operating system that defines how the terminal will behave and looks after running (or executing) commands for you. There are various shells available but the most common one is called bash which stands for Bourne again shell. This tutorial will assume you are using bash as your shell.

If you would like to know which shell you are using you may use a command called echo to display a system variable stating your current shell. echo is a command which is used to display messages.

## Basic Navigation

<https://ryanstutorials.net/linuxtutorial/navigation.php>

pwd which stands for Print Working Directory. The command does just that. It tells you what your current or present working directory is.

ls [options] [location]

ls
bin Documents public_html
ls -l
total 3
drwxr-xr-x  2 ryan users 4096 Mar 23 13:34 bin
drwxr-xr-x 18 ryan users 4096 Feb 17 09:12 Documents
drwxr-xr-x  2 ryan users 4096 May 05 17:25 public_html
ls /etc
a2ps.cfg aliases alsa.d cups fonts my.conf systemd
...
ls -l /etc
total 3
-rwxr-xr-x  2 root root 123 Mar 23 13:34 a2ps.cfg
-rwxr-xr-x 18 root root 78 Feb 17 09:12 aliases
drwxr-xr-x  2 ryan users 4096 May 05 17:25 alsa.d
...
Let's break it down:

Line 1 - We ran ls in it's most basic form. It listed the contents of our current directory.
Line 4 - We ran ls with a single command line option ( -l ) which indicates we are going to do a long listing. A long listing has the following:
First character indicates whether it is a normal file ( - ) or directory ( d )
Next 9 characters are permissions for the file or directory (we'll learn more about them in section 6).
The next field is the number of blocks (don't worry too much about this).
The next field is the owner of the file or directory (ryan in this case).
The next field is the group the file or directory belongs to (users in this case).
Following this is the file size.
Next up is the file modification time.
Finally we have the actual name of the file or directory.
Line 10 - We ran ls with a command line argument ( /etc ). When we do this it tells ls not to list our current directory but instead to list that directories contents.
Line 13 - We ran ls with both a command line option and argument. As such it did a long listing of the directory /etc.
Lines 12 and 18 just indicate that I have cut out some of the commands normal output for brevities sake. When you run the commands you will see a longer listing of files and directories.

### Absolute and Relative Paths

At the very top of the structure is what's called the root directory. It is denoted by a single slash ( / ). It has subdirectories, they have subdirectories and so on. Files may reside in any of these directories.

Absolute paths specify a location (file or directory) in relation to the root directory. You can identify them easily as they always begin with a forward slash ( / )

Relative paths specify a location (file or directory) in relation to where we currently are in the system. They will not begin with a slash.

Relative paths specify a location (file or directory) in relation to where we currently are in the system. They will not begin with a slash.

More on Paths

You'll find that a lot of stuff in Linux can be achieved in several different ways. Paths are no different. Here are some more building blocks you may use to help build your paths.

~ (tilde) - This is a shortcut for your home directory. eg, if your home directory is /home/ryan then you could refer to the directory Documents with the path /home/ryan/Documents or ~/Documents
. (dot) - This is a reference to your current directory. eg in the example above we referred to Documents on line 4 with a relative path. It could also be written as ./Documents (Normally this extra bit is not required but in later sections we will see where it comes in handy).
.. (dotdot)- This is a reference to the parent directory. You can use this several times in a path to keep going up the hierarchy. eg if you were in the path /home/ryan you could run the command ls ../../ and this would do a listing of the root directory.


## More About Files

<https://ryanstutorials.net/linuxtutorial/aboutfiles.php>

Everything is a File

Ok, the first thing we need to appreciate with linux is that under the hood, everything is actually a file. A text file is a file, a directory is a file, your keyboard is a file (one that the system reads from only), your monitor is a file (one that the system writes to only) etc. To begin with, this won't affect what we do too much but keep it in mind as it helps with understanding the behaviour of Linux as we manage files and directories.

Linux is an Extensionless System

A file extension is normally a set of 2 - 4 characters after a full stop at the end of a file, which denotes what type of file it is. The following are common extensions:

file.exe - an executable file, or program.
file.txt - a plain text file.
file.png, file.gif, file.jpg - an image.

**file**
obtain information about what type of file a file or directory is.
**ls -a**
List the contents of a directory, including hidden files.
**Everything is a file under Linux**
Even directories.
**Linux is an extensionless system**
Files can have any extension they like or none at all.
**Linux is case sensitive**
Beware of silly typos.

## Manual Pages

<https://ryanstutorials.net/linuxtutorial/manual.php>

## File Manipulation

<https://ryanstutorials.net/linuxtutorial/filemanipulation.php>

**mkdir**
Make Directory - ie. Create a directory.
**rmdir**
Remove Directory - ie. Delete a directory.
**touch**
Create a blank file.
**cp**
Copy - ie. Copy a file or directory.
**mv**
Move - ie. Move a file or directory (can also be used to rename).
**rm**
Remove - ie. Delete a file.
**No undo**
The Linux command line does not have an undo feature. Perform destructive actions carefully.
**Command line options**
Most commands have many useful command line options. Make sure you skim the man page for new commands so you are familiar with what they can do and what is available.

## Cheat Sheet

<https://ryanstutorials.net/linuxtutorial/cheatsheet.php>

### Basic Nav

pwd
Where am I in the system.
ls [path]
Perform a listing of the given path or your current directory.
Common options: -l, -h, -a
cd [path]
Change into the given path or into your home directory.
Path
A description of where a file or directory is on the filesystem.
Absolute Path
One beginning from the root of the file system (eg. /etc/sysconfig ).
Relative Path
One relative to where you currently are in the system (eg. Documents/music ).
~ (tilde)
Used in paths as a reference to your home directory (eg. ~/Documents ).
. (dot)
Used in paths as a reference to your current directory (eg. ./bin ).
.. (dot dot)
Used in paths as a reference to your current directories parent directory (eg. ../bin ).
TAB completion
Start typing and press TAB. The system will auto complete the path. Press TAB twice and it will show you your alternatives.

### File shortcuts

file [path]
Find out what type of item a file or directory is.
Spaces in names
Put whole path in quotes ( " ) or a backslash ( \ ) in front of spaces.
Hidden files and directories
A name beginning with a . (dot) is considered hidden.

### File Manip

mkdir < directory name>
Create a directory
rmdir < directory name>
Remove a directory (only if empty).
touch < file name>
Create a blank file.
cp < source> < destination>
Copy the source file to the destination.
mv < source> < destination>
Move the source file to the destination.
May also be used to rename files or directories.
rm < path>
Remove a file or directory.
Common options: -r -f

Summarizing your observations and learnings, highlighting things like your ‘ah hah’ moments or really interesting code snippets.

I thought the reading was a really good review of past learnings put into nice bite size pieces for easy reference.
