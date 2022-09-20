# Course 102 Class 2 "The Coder's Computer" Reading Notes

## *Class Two*

**Text Editor:**
A text editor is a piece of software that you download and install on
your computer, or you access online through your web browser, that
allows you to write and manage text, especially the text that you write
to build a web site.

What features should you look for in a text editor? I would say some
of the most important features are:

- code completion
- syntax highlighting
- a nice variety of themes (to reduce eye strain and fatigue)
- the ability to choose from a healthy selection of extensions available when you need them.

### LINUX IS CASE SENSITIVE

**Basic Linux Commands:**

- pwd: Print Working Directory - ie. Where are we currently.
- ls: List the contents of a directory.
- cd: Change Directories - ie. move to another directory.

**Paths:**

Absolute paths: specify a location (file or directory) in relation to the root directory. You can identify them easily as they always begin with a forward slash ( / )

Relative paths: specify a location (file or directory) in relation to where we currently are in the system. They will not begin with a slash.

~ (tilde): - This is a shortcut for your home directory. eg, if your home directory is /home/ryan then you could refer to the directory Documents with the path /home/ryan/Documents or ~/Documents

. (dot): - This is a reference to your current directory. eg in the example above we referred to Documents on line 4 with a relative path. It could also be written as ./Documents (Normally this extra bit is not required but in later sections we will see where it comes in handy).

.. (dotdot):- This is a reference to the parent directory. You can use this several times in a path to keep going up the hierarchy. eg if you were in the path /home/ryan you could run the command ls ../../ and this would do a listing of the root directory.

In order to move around in the system we use a command called cd which stands for change directory. It works as follows:

cd [location] (If you run the command cd without any arguments then it will always take you back to your home directory.)

**FILES:**

Ok, the first thing we need to appreciate with linux is that under the hood, everything is actually a file. A text file is a file, a directory is a file, your keyboard is a file (one that the system reads from only), your monitor is a file (one that the system writes to only) etc. To begin with, this won't affect what we do too much but keep it in mind as it helps with understanding the behaviour of Linux as we manage files and directories.

- file.exe - an executable file, or program.
- file.txt - a plain text file.
- file.png, file.gif, file.jpg - an image.

 **Spaces In Names:**
Spaces in file and directory names are perfectly valid but we need to be a little careful with them. As you would remember, a space on the command line is how we seperate items. They are how we know what is the program name and can identify each command line argument. If we wanted to move into a directory called Holiday Photos for example the following would not work. $ cd Holiday Photos

What happens is that Holiday Photos is seen as two command line arguments. cd moves into whichever directory is specified by the first command line argument only. To get around this we need to identify to the terminal that we wish Holiday Photos to be seen as a single command line argument. There are two ways to go about this, either way is just as valid.

Quotes:
The first approach involves using quotes around the entire item. You may use either single or double quotes (later on we will see that there is a subtle difference between the two but for now that difference is not a problem). Anything inside quotes is considered a single item.    cd 'Holiday Photos'

Escape Characters:
Another method is to use what is called an escape character, which is a backslash ( \ ). What the backslash does is escape (or nullify) the special meaning of the next character.
cd Holiday\ Photos

**Hidden Files or Directories:**

To make a file or directory hidden all you need to do is create the file or directory with it's name beginning with a . or rename it to be as such. Likewise you may rename a hidden file to remove the . and it will become unhidden. The command ls which we have seen in the previous section will not list hidden files and directories by default. We may modify it by including the command line option -a so that it does show hidden files and directories.

ls Documents

FILE1.txt File1.txt file1.TXT

ls -a Documents

FILE1.txt File1.txt file1.TXT .hidden .file.txt

ls -a Command is used to List the contents of a directory, including hidden files.

Return to the Table of Contents: [Table of Contents](https://todd75.github.io/reading-notes/courses)