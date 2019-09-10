# Basics Cheet Sheet


### ls
---
List files

This command is used to show the files that are in the current directory, another directory, or files that match some pattern.

```bash
marshall@cerberus:bash-intro (master)$ ls
CheetSheet.md	LICENSE		README.md	testDir
````

`ls [flags] [files ...]`

Below is a table showing some of the arguments that can be used

| flag | description |
| ---- | ----- |
| `-a` | show hidden files |
| `-l` | show details of the file |
| `-G` or `--color` |  color the output by file type|


### cd
---
Change Directory

This command can be used to navigate to another directory.

```bash
marshall@cerberus:~/bash-intro$ cd testDir
marshall@cerberus:~/bash-intro/testDir$ 
````

`cd path`

There are some special location symbols

| symbol | meaning |
| ----- | ------- |
| `~` | home directory |
| `.` | current directory |
| `..` | parrent direcotry |
| `/` | root (top) directory|
| `-` | previous directory |


### touch
---
Create file

This is a simple command to create a file, or update its modification time.

```bash
marshall@cerberus:~/bash-intro/testDir$ ls
marshall@cerberus:~/bash-intro/testDir$ touch awsomeFile.txt
marshall@cerberus:~/bash-intro/testDir$ ls
awsomeFile.txt
marshall@cerberus:~/bash-intro/testDir$
````

`touch fileName`


### mkdir
---
Create Directory

This command can be used to create a new directories

```bash

marshall@cerberus:~/bash-intro$ ls
marshall@cerberus:~/bash-intro$ mkdir folder
marshall@cerberus:~/bash-intro$ ls
folder
````

`mkdir name`

If the name contains other directories that do not yet exist they can be created as well by using the `-p` flag. 


### rm
---
Remove

This command is potentially dangerous and can be used to remove files and folders

```bash

marshall@cerberus:~/bash-intro$ ls
deleteMe.txt
marshall@cerberus:~/bash-intro$ rm deleteMe.txt
marshall@cerberus:~/bash-intro$ ls
marshall@cerberus:~/bash-intro$
````

`rm [flags] names`


Below is a table showing some of the arguments that can be used

| flag | description |
| ---- | ----- |
| `-f` | attempt to delete it forcefully, dont ask for confirmation |
| `-r` or `-R` | recursive, delete all the files in the folders too |




### cat
---
Print files

This is a simple command to print the contents of a file

```bash
marshall@cerberus:~/bash-intro/$ ls
CheetSheet.md LICENSE       README.md     testDir
marshall@cerberus:~/bash-intro$ cat README.md 
# bash-intro
Content  for the into to bash workshop
awsomeFile.txt
marshall@cerberus:~/bash-intro/testDir$
````

`cat fileName ...` 

If you want to show line numbers in the output the `-n` flag can be used. 


### echo
---
White to stdout

This command will output what ever you give it to the screen. Its usefull for printing variables, or piping strings into other functions (more on this later). 

```bash
marshall@cerberus:~/bash-intro/$ echo "Hey there"
Hey there
marshall@cerberus:~/bash-intro$ echo "$HOME"
/Users/marshall
marshall@cerberus:~/bash-intro/testDir$ 
````

`echo string ...`
