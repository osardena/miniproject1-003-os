# **Basic Linux and Vi Commands Needed to Manage a File System**

First, let's go over 11 basic Linux commands to manage a file system.

## **1. cd [change directory]** 

cd is the "change directory" command, used for changing the current working directory that you are in. A directory is essentially like a folder, which may contain files and other directories. Your current working directory is the "folder" in which you are currently in.

To use the cd command, type on the terminal cd and then the path of the directory you want to change into, in this format: **cd directorypath**. It is important to put a space between the command and the argument passed into it.

The following are some common cd commands:
* **cd /**: this command takes changes you into the root directory--the first file directory in your filesystem hierarchy.
* **cd /directory1/directory2/directory3**: This commands takes you inside a subdirectory in another directory.
    * For example: cd /home/student/Documents/ would take you to the Documents directory inside the student directory
    * If you are already in a directory and want to travel into a subdirectory, you would not have to provide the full path to that directory. Instead, you can provide the relative path
        * If there was a subdirectory called Projects in the Documents directory you were already in, you would only need to type 'cd Projects' to change into that directory.

* The cd ~ and **cd** commands take you to your home directory, no matter what your current working directory is.

* **cd ..** changes you into the parent directory--that is the directoy one level up from the directory you are in.
    * From the previous example, if your current working directory is Projects, then typing **cd ..** would take you back to the Documents directory.

## **2. pwd [print working directory]**

pwd is the "print working directory" command, used for display the current directory the user is in. It is a useful command when unsure of the directory you are in or to view the full path of your directory. To use it, simply type pwd on the command line and it will display the full path of your current directory.

