# Learn command line

Please follow and complete the free online [Command Line Crash Course
tutorial](https://web.archive.org/web/20160708171659/http://cli.learncodethehardway.org/book/) or [Codecademy's Learn the Command Line](https://www.codecademy.com/learn/learn-the-command-line). These are helpful tutorials. Each "chapter" focuses on a command. Type the commands you see in the _Do This_ section, and read the _You Learned This_ section. Move on to the next chapter. You should be able to go through these in a couple of hours.

---

### Q1.  Cheat Sheet of Commands  

Here's a list of items with which you should be familiar:  
* show current working directory path
* creating a directory
* deleting a directory
* creating a file using `touch` command
* deleting a file
* renaming a file
* listing hidden files
* copying a file from one directory to another

Make a cheat sheet for yourself: a list of at least **ten** commands and what they do.  (Use the 8 items above and add a couple of your own.)  

* `pwd`    : current working directory
* `mkdir`  : creating a directory
* `rmdir`  : removing directory
* `touch`  : creating a file (type nul > filename.txt)
* `del`    : delete a file
* `ren`    : renaming a file
* `ls -a`  : list hidden files  (dir /AH show only hidden files)
* `copy`   : copying files from one directory to another (use full path)
* `cd ~`   : go back to home directory
* `exit`   : exit the shell
    
    

---

### Q2.  List Files in Unix   

What do the following commands do:  
`ls`  
`ls -a`  
`ls -l`  
`ls -lh`  
`ls -lah`  
`ls -t`  
`ls -Glp`  

    * `ls`      : lists all the files in the directory
    * `ls -a`   : list hidden files and directories
    * `ls -l`   : list with long format - show permissions
    * `ls -lh`  : list long format with readable file size
    * `ls -lah` : list long format  with readable file size including hidden files
    * `ls -t`   : sort by time and date
    * `ls -Glp` : list all files, exclude owner name, display directories with a /

---

### Q3.  More List Files in Unix  

Explore these other [ls options](http://www.techonthenet.com/unix/basic/ls.php) and pick 5 of your favorites:

    * `ls -c`   : displays files by file timestamp
    * `ls -R`   : displays subdirectories as well
    * `ls -x`   : displays files as rows across the screen
    * `ls -1`   : displays each entry on a line
    * `ls -q`   : displays all nonprinting characters as ?

---

### Q4.  Xargs   

What does `xargs` do? Give an example of how to use it.

    It is used to build and execute command lines from standard input (STDIN)
    Example-
    `echo 1 2 3 4 | xargs -n 2`
    This line prints the numbers, limiting the number of entries in a line to 2

 

