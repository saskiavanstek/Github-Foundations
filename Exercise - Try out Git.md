# Exercise - Try out Git

Before you can create your first repo, you must make sure that Git is installed and configured. 
Git comes preinstalled with Azure Cloud Shell. 
If you are using a local command line, it might be necessary to install Git.

## Check if Git is installed

In the Cloud Shell, or your locall Command Line type the command below to double-check that Git is installed

```
git --version

```
You should see output that looks something like this example:

```
git version 2.7.4
```
To configure Git, you must define some global variables: **user.name** and **user.email**
Both are required for you to make commits

## Set you user.name and user. email

Set you name with the following command 
Replace **<USER_NAME>** with the user name you want to use

```
git config --global user.name "<USER_NAME>"
```
Now use the below command to create a **user.email** configuration variable, replacing **<USER_EMAIL>** with your e-mail address

```
git config --global user.email "<USER_EMAIL>"

```
Run the following command to check that your changes worked

```
git config --list

```
Confirm that the output includes two lines that are similar to the below example. 
Your name and e-mail addresss will be different from what's shown in this example.

```
user.name=User Name
user.email=user-name@domain.com

```

## Set up your Git Repository

Git works by checking for changes to files within a certain folder. 
We will create a folder to serve as our _working tree_ (project directory) and let Git know about it, so it can start tracking changes.
We tell Git to start tracking by initializing a Git repository into that folder.

Start by creating and empty folder for your project, and then initialize a Git repo inside it. 

1. Create a folder named _Cats_. This filder wil be the project directory, also called the working tree. The project directory is where all files related to your project are stored. 
```
mkdir Cats
```
2. Change to the project directory by using the **cd** command
```
cd Cats
```
3. Now initialize your new repository and set the name of the default branch to **main**
   If you're running Git version 2.28.0 or later, use the following command:
   ```
   git init --initial-branch=main
   ```
   or use the following command:
   ```
   git init -b main
   ```
   For earlier versions of Git use these commands
   ```
   git init
   git checkout -b main
   ```
4. Now, use a **git status** command to show the status of the working tree
   ```
   git status
   ```
   Git responds with the below output, which indicates that **main** is the current branch.
   ```
   On branch main

   No commits yet

   ```
5. Use an **ls** command to show the contents of the working tree
   ```
   ls -a
   ```
> [!NOTE]
> If you are working in Windows PowerShell **ls -a** will give an error message. Instead use **ls -hidden**

> [!TIP]
>Confirm that the directory contains a subdirectory named _.git_ (Using the -a option with ls is important because Linux normally hides file and directory names that starts with a period)
>This folder is the Git repository. The directory in which Git stores metadata and history for the working tree.
>
>You typically don't do anything with the _.git_ directory directly. Git updates the metadata there as the status of the working tree changes to keep track of what's changed in your files. 
>This directory is hands-off for you, but it's incredibly important to Git.

## Get help from git

Git like most command-line tools, has a built-in help function that you can sue to look up commands and keywords.

1. Type the following command to get help with what you can do with Git

```
git --help
```
2. The command displays the following output
```
usage: git [--version] [--help] [-C <path>] [-c name=value]
       [--exec-path[=<path>]] [--html-path] [--man-path] [--info-path]
       [-p | --paginate | --no-pager] [--no-replace-objects] [--bare]
       [--git-dir=<path>] [--work-tree=<path>] [--namespace=<name>]
       <command> [<args>]

These are common Git commands used in various situations:

start a working area (see also: git help tutorial)
   clone      Clone a repository into a new directory
   init       Create an empty Git repository or reinitialize an existing one

work on the current change (see also: git help everyday)
   add        Add file contents to the index
   mv         Move or rename a file, a directory, or a symlink
   reset      Reset current HEAD to the specified state
   rm         Remove files from the working tree and from the index

examine the history and state (see also: git help revisions)
   bisect     Use binary search to find the commit that introduced a bug
   grep       Print lines matching a pattern
   log        Show commit logs
   show       Show various types of objects
   status     Show the working tree status

grow, mark and tweak your common history
   branch     List, create, or delete branches
   checkout   Switch branches or restore working tree files
   commit     Record changes to the repository
   diff       Show changes between commits, commit and working tree, etc
   merge      Join two or more development histories together
   rebase     Forward-port local commits to the updated upstream head
   tag        Create, list, delete or verify a tag object signed with GPG

collaborate (see also: git help workflows)
   fetch      Download objects and refs from another repository
   pull       Fetch from and integrate with another repository or a local branch
   push       Update remote refs along with associated objects

'git help -a' and 'git help -g' list available subcommands and some
concept guides. See 'git help <command>' or 'git help <concept>'
to read about a specific subcommand or concept.

 ```
 
> [!TIP]
> Read through the different options available with Git and note that each command comes with its own help page, for when you start digging deeper. Not all these commands will make sense yet, but some might look familiar if you have experience using VCS.
> In the next lessons, you will learn more about the commands you just tried and the basics of Git.



  
