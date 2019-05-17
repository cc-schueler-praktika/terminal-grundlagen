# Bash Cheat Sheet

## Intro 👋

In a Linux system, the *shell* is a command-line interface that interprets a user's commands and script files, and tells the server's operating system what to do with them.

This document was written using the *Bourne-Again shell*, usually referred to as `bash`, which is the default shell for most Linux distributions, including Ubuntu, CentOS, and RedHat.

When you first login to a server, you will be dropped into the command prompt, or shell prompt, which is where you can issue commands to the server. The information that is presented at the command prompt can be  customized by the user, but here is an example command prompt:

```bash
sammy@webapp:~$     # <username>@<hostname>:<current-directory><promptSymbol>
```

A german cheat sheet is available here: https://bit.ly/2bSDxyT [Wiki ubuntuusers]



## Commands 🛠

#### without arguments or options

```bash
cd     # you will be returned to your current user's home directory
ls     # will print a listing of the current directory's files and directories
touch  # will print a message that shows you how to use the 'touch' command
```

#### with arguments

```bash
mkdir code  # will create a directory named 'code' (mkdir => "make directories")
cd code     # will change to the code directory (cd => "change directory")
```

#### with options

```bash
ls -l   # print a "long listing", which includes extra details
ls -a   # list "all" of a directory's files, including hidden ones (that start with .)
```

```bash
ls -l -a   # options can be grouped together
ls -la     # options can be combined (short form for '-l -a')
```

#### with options and arguments

```bash
ls -la code   # options and arguments can be combined 
```



## Help 💡

```bash
man ls       # show manual page for 'ls' command
man --help   # show short description of 'man' command
```



## Navigation and Exploration 🕵️‍♀️

```bash
pwd   # display the directory you are currently in
```

```bash
cd /home/tina/code   # change to directory using an absolut path
cd tina/code         # change to directory using a relative path
cd code              # change to directory within the current directory
```



## File and Directory Manipulation 📄

**Note**: It is important to realize that your Linux system will not prevent you from certain destructive actions.  If you are renaming a file and choose a name that *already* exists, the previous file will be **overwritten** by the file you are moving.  There is no way to recover the previous file if you accidentally overwrite it.

```bash
touch file1               # create an empty file
touch file2 file3 file4   # create multiple files at the same time
```

```bash
mkdir notes                    # create a directory named 'notes'
mkdir notes/internship         # create a directory within the already existing directory 'notes'
mkdir -p some/other/directory  # create a directory structure
```

```bash
mv file1 /home/tina/code   # move 'file1' to code directory
mv /home/tina/file2 .      # move 'file2' to current directory (.)
mv file2 fileWithName      # rename 'file2' to 'fileWithName'
```

```bash
cp file1 copyOfFile1          # copy 'file1' to a new file 'copyOfFile1'
cp -r notes/dir1 notes/dir2   # copy 'dir1' directory to a new directory 'dir2'
```

```bash
rm file1              # delete file named 'file1'
rmdir notes/dir1      # delete empty directory named 'dir1'
rmdir -r notes/dir2   # remove directory 'dir2' and all files and directories within it
```

```bash
chmod +x sample.py   # make file 'sample.py' executable for all users
```



## Thanks! 👏

[1] https://www.digitalocean.com/community/tutorials/an-introduction-to-the-linux-terminal

[2] https://www.digitalocean.com/community/tutorials/basic-linux-navigation-and-file-management
