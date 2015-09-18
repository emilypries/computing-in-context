# COMS1002 - Computing in Context
Information for the Digital Humanities discussion section.

### Recitation 2
9/18/15 - Today we are setting up our personal web pages and practicing writing and executing Python scripts. The instructions for setting up your web page are on Courseworks under Syllabus -> "Files, Unix, and making a webpage."

Three practice programs follow:
- [Edsger and the Philosophers](#edsger-and-the-philosophers)
- [Richards GNU Zoo](#richards-gnu-zoo)
- [Grace Bugs Out](#grace-bugs-out)

###### Edsger and the Philosophers
Edsger is planning a dinner party for five Dining Philosophers, but he has no forks. Unfortunately, the philosophers are all silent, so he needs your help to write a program to communicate with them. Design a program that allows him to individually ask each philosopher how many forks they will bring to the dinner party and then tell Edsger how many total forks he can expect.

Follow up questions:
- What are you assuming about the input?
- Are your assumptions valid?
- What is the most useful format for output?

Creative step:
- Modify your program to provide more information of your choosing. You are welcome to collect further input. Possibilities include:
	- Average number of forks per philosopher
	- The number of tines the philosophers will bring
	- The maximum (or minimum) number of forks a philosopher will bring
	- How many forks too many or too few will there be?
- Modify your program in a way of your choosing!

Bonus:
- Who is Edsger?
- Who are the Dining Philosphers?

###### Richard's GNU Zoo
Richard started a gnu zoo in 1983. Every year, he gets 10 new gnus. Write a program that calculates how many gnus are in Richard's gnu zoo in a given year (must take year as input).

Follow up questions:
- What are you assuming about the input?
- Are your assumptions valid?
- What is the most useful format for output?

Creative step:
- Modify your program to account for an annual death rate of 10% of the current pack.
	- Can you have a fraction of a gnu?
- Modify your program to calculate how many gnus would be in the zoo if the pack doubled every year.
- Modify your program to calculate the average age of gnu (this is much easier if you do not include a death rate)
- Modify your program in a way of your choosing!

Bonus:
- Who is Richard?
- What is GNU? Why 1983?

###### Grace Bugs Out
Grace wants to catch a moth that she sees every day at 7:00PM. Write a program that tells Grace how long until she can see the moth given a time as input (you can decide how Grace must write the time).

Follow up questions:
- What are you assuming about the input?
- Are your assumptions valid?
- What is the most useful format for output?

Creative step:
- Modify your program to also tell her how long it has been since she last saw the moth.
- Modify your program to allow Grace to also input a new time that the moth will appear and calculate accordingly.
- Grace first saw the moth on January 1st, 1947, and has seen it daily since. Write a program that takes a year as input and calculates how many times she has seen the moth.
- Modify your program in a way of your choosing!

Bonus:
- Who is Grace?
- What moth-related term did she coin, and what does it mean?



### Recitation 1
9/11/15 - Today we are setting up our computers so that we can spend the semester having fun writing code instead of worrying about where our files are saved or why we can't run a program. We will:

- Learn [bash commands](#basic-terminal-commands) to navigate through Terminal
- [Install Anaconda](#installing-anaconda)
- [Install Cyberduck](#installing-cyberduck) (Mac) or [MobaXterm](#installing-mobaxterm) (Windows)

#### Basic Terminal Commands
Using Terminal on a Mac or a Windows Command Prompt lets you interact with your files quickly and send commands directly to your system. Although the functionality is similar between Mac and Windows, the terms are slightly different. In both cases, we use "directory" to mean folder and interact with files and directories by typing commands and pressing "Enter".

To open a Command Prompt on a Windows machine, click start, choose Run..., and type "cmd" (or "command").
To open Terminal on a Mac, open your Applications folder, open the "Utilities" folder, and open Terminal.

HINT: When typing the name of a file or directory, press Tab to auto-complete.

###### Current Working Directory
To find out which directory you have open right now, on a Mac, type ```pwd``` (which stands for present working directory), and on Windows, type ```cd``` (which stands for current directory).

###### List files
To list all the files (and directories) in your current directory, on a Mac, type ```ls```, and on Windows, type ```dir```.

###### Change Directory
To navigate to another directory, on both Mac and Windows, type ```cd <directory_name>``` (cd stands for change directory). Here, <directory_name> can either be the name of a directory within your current working directory or the path to another directory on your computer.

For example, if I'm currently in a directory called Documents, which contains a directory called School, I can type ```cd School``` (or ```cd School/``` - the trailing slash does not matter here), and my current working directory will now be School.

The path of a directory is the list of directories that contain it. In the example above, the path to my School directory would be Documents/School. If I have a 1002 directory in my School directory, its path would be Documents/School/1002.

This is handy, because if my current working directory if Documents but I want to be in my 1002 directory, I can type ```cd School/1002``` instead of ```cd School``` then ```cd 1002```.  I didn't type ```cd Documents/School/1002``` here, even though School is in the Documents directory, because paths are _relative_ to which directory you are currently in. (You can change to any directory by specifying its full path, but we won't get into that today - as will often be the case in this class, I encourage you to Google search for more info if you're curious!).

###### Up One Level
If you're currently in a sub-directory and want to move up one level to its parent (in the example above, from School back to Documents), on a Mac type ```cd ..```, and on Windows type ```cd..```.

###### Make a New Directory
To make a new directory within your current working directory, on a Mac type ```mkdir <name_of_new_directory>```, and on Windows type ```md <name_of_new_directory>```, where <name_of_new_directory> is replaced by (surprise!) the name you want to call your new directory.

###### Text Editing
In addition to Text Edit, Notepad, and other word processing applications you've used before, you can edit text directly from your terminal. There are a variety of terminal text editors (you might hear "vim" and "emacs" in particular), but pico is a straightforward one that reminds you how to use it. It comes installed on many machines and is available on CUNIX.

To open a text file, type ```pico <file_name.txt>``` (for example, test.txt). Type whatever you wish, and use the commands at the bottom of the screen to save (the ^ character represents control). To exit, press ctrl-x. It will ask if you want to save; type ```y``` to save, and enter to confirm the file name.

You just created a text file in your current directory - how might you list the files to make sure it's there?

These are just the basics, but these will be the majority of the commands we use in this class. There are lots of other commands and plenty of resources online to help you discover and learn them.

#### Installing Anaconda
Anaconda is a Python distribution that includes useful tools and libraries, several of which we will take advantage of throughout this course.

1. Open the [Anaconda download page](http://continuum.io/downloads).
2. IMPORTANT: Choose the blue "I WANT PYTHON 3.4*" link.
3. Download the appropriate installer for your operating system (Mac/Windows/Linux).
4. Open the installer and follow the instructions, as described [here](http://docs.continuum.io/anaconda/install). When it asks, modify your PATH variable as directed (or don't... I'm assuming if you don't want to, you know what you're doing here. Either way it's reversible).
5. After you get a successful installation message, open a _new_ terminal window and type ```conda info```. You will know that you have a successful installation if you get helpful information instead of an error. Double check that the python version listed is 3.4, not 2.7.

#### Installing Cyberduck
Cyberduck is a tool that makes it easy to connect your computer to another computer and transfer or interact with files that are stored there. We'll use it move files from our own computers to Columbia's [CUNIX system](http://www.columbia.edu/~lgw23/cs1004/). Today, we'll install Cyberduck and make sure we can transfer files successfully.

1. Open the [Cyberduck website](https://cyberduck.io/).
2. Click to download the Mac version (it will be a .zip file instead of a .exe).
3. Open the .zip file and follow the instructions to install Cyberduck. Move it to your Applications folder so that it is easy to find.
4. Open Cyberduck and click the "Open Connection" button on the top left.
5. From the drop-down menu on the top, choose "SFTP (SSH File Transfer Protocol)". This tells Cyberduck [how](https://en.wikipedia.org/wiki/SSH_File_Transfer_Protocol) we want to communicate with the CUNIX server.
6. In the "Server" box, type "cunix.columbia.edu". Keep the "Port" field at 22.
7. Fill in the "Username" and "Password" boxes with your UNI information.
8. Click "Connect".

Success! You can now interact with your CUNIX files just as you would through Finder: try dragging and dropping to copy files back and forth from your computer to CUNIX, double-clicking to open files, or dragging to move a file into a folder.

#### Installing MobaXterm
MobaXterm is a tool that makes it easy to connect your computer to another computer and transfer or interact with files that are stored there. We'll use it move files from our own computers to Columbia's [CUNIX system](http://www.columbia.edu/~lgw23/cs1004/). Today, we'll install MobaXterm and make sure we can transfer files successfully.

1. Open the [MobaXterm website](http://mobaxterm.mobatek.net/).
2. Click the orange "Get MobaXterm Now!" button and download the free home edition of MobaXterm. The green "Installer edition" will likely be easier for most people to install, but if it doesn't work for you (for example, because your computer has complicated permissions set up), try the blue "Portable edition".
3. Open the installer and follow the instructions to install MobaXterm. Installing to your Applications folder will make it easy to find.
4. Open MobaXterm, click the "Session" button on the top left, and choose "New Session".
5. From horizontal icons on top, click the "SSH".
6. In the "Remote host" box, type "cunix.columbia.edu".
7. Check the "Specify username" and enter your UNI. Keep the Port at 22.
8. Click "OK" and you will be prompted for your password - this is your same UNI password.

Success! You can now interact with your CUNIX files on the pane on the left just as you would through Finder: try dragging and dropping to copy files back and forth from your computer to CUNIX, double-clicking to open files, or dragging to move a file into a folder.

