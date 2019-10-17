# **Basic Linux and Vi Commands Needed to Manage a File System**

## 7 Basic Linux Commands to Manage a File System.

### **1. cd [change directory]** 

`cd` is the "change directory" command, used for changing the current working directory that you are in. A directory is essentially like a folder, which may contain files and other directories. Your current working directory is the "folder" in which you are currently in.

To use the cd command, type on the terminal cd and then the path of the directory you want to change into, in this format: `cd directorypath`. It is important to put a space between the command and the argument passed into it.

The following are some common cd commands:
* `cd /`: this command takes changes you into the root directory--the first file directory in your filesystem hierarchy.
* `cd /directory1/directory2/directory3`: This commands takes you inside a subdirectory in another directory.
    * For example: `cd /home/student/Documents/` would take you to the Documents directory inside the student directory
    * If you are already in a directory and want to travel into a subdirectory, you would not have to provide the full path to that directory. Instead, you can provide the relative path
        * If there was a subdirectory called Projects in the Documents directory you were already in, you would only need to type 'cd Projects' to change into that directory.
* The `cd ~` and `cd` commands take you to your home directory, no matter what your current working directory is.
* `cd ..` changes you into the parent directory--that is the directoy one level up from the directory you are in.
    * From the previous example, if your current working directory is Projects, then typing `cd ..` would take you back to the Documents directory.

### **2. pwd [print working directory]**

`pwd` is the "print working directory" command, used for display the current directory the user is in. It is a useful command when unsure of the directory you are in or to view the full path of your directory. To use it, simply type `pwd` on the command line and it will display the full path of your current directory.

### **3. mkdir [make directoy]**

`mkdir` is the "make directory" command, used for making a new directory. To use it, type mkdir, a space, and the name of the new directory you wish to create: `mkdir nameofnewdirectory`. Again, it is important to add a space between the command and the argument passed to it. 
* Note: `mkdir nameofnewdirectory` will create that new directory inside of your current working directory.
   * If you wish to create a directory outside of your current working directory, you can type mkdir, followed by a space, and then the full path of the new directory. 
       * For example, if one wanted to create a new directory named 'Homework' inside the Documents directory, one would type: `mkdir /home/student/Documents/Homework`

### **4. cp [copy]**

`cp` is the "copy" command, used for making copies of the content of files and directories. It creates an exact copy of the contents in the files/directories. The syntax for the cp command is: `cp [option] source destination` where **source** is the file you want to copy and **destination** is where you want to copy it to. Copies the files with the same name!
* Note: source and destination can be directories or files
* There are many options that can be used along with the cp command. To read about them all, you can type `man cp` on your command line. 
   * Some common ones are:
      * **-v** - Be verbose. Shows the files are they are being copied
      * **-n** - Do not overwrite an existing file
      * **-i** - Causes cp to write a prompt to the standard error output before copying a file that would overwrite an existing file.
     * **-p** - Preserves the modification time, access time, file flags, file mode, user ID, and group ID, as allowed by permissions, in the copy.
* Using cp with two files
   * `cp file1 file2` - copies the contents of **file1** to the **file2**. 
      * If **file2** doesn't exist, then it will create a file with that name. However, if that file exists, it will overwrite the contents of that file.
* Using cp with two directories
   * `cp -R dir1 dir2` - copies the contents and subdirectories in **dir1** onto **dir2**. 
      * It is necessary to use the -R option (causes cp to be recursive and copy any and all subdirectories)   
* Copying two or more files
   * `cp file1 file2 file3 directory` - copies **file1, file2, and file3** into **directory**.
      * If *directory* does not exist, it will create one. But if it does exist, it will overwrite it.
      
 ### **5. mv [move files]**
 
`mv` is the move command, used to move a file or directory to a different location. Unlike `cp`, which copies a file/directory onto a different location and leaves the original file where it is, `mv` moves the original to a different location and deletes it from where it previously was. 

To syntax to use the `mv` command is: `mv [option] source destination`. where **source** is the file you want to copy and **destination** is where you want to copy it to.
* Note: You can also use `mv` to rename files. The syntax for that is: `mv fileyouwanttorename newname`
   * Example:
      ```
         $ls
         file1    file2    file3
         $mv file1 newNameForFile1
         $ls
         file2 file3 newNameForFile1
      ```
* [options] can be found by typing `man mv` on the command line.

### **6. rm [remove]**

`rm` is the remove command, used to remove directories entries. Be careful when using this command because once you remove files, you cannot recover them.
* Syntax:
   * To delete a file: `rm filename` where **filename** is the name of the file you want to delete
   * To delete multiple files: `rm file1 file2 file3 file4`
   * To delete **empty** directories: `rm -d directoryname` or `rmdir directoryname`
      * Emphasis on empty!
   * To delete **all** the files and sub-directories in a directory: `rm -r directoryname`
*More syntax options can be found by typing `man rm` on the command line*


### 7. history

The `history` command is used to display the last 500 commands invoked in your account. To use it, simply type `history` on your command line.
* You can invoke any of the commands shown in the history by typing the ‘!’ followed by the command number
* The command `history –c` clears the history buffer
