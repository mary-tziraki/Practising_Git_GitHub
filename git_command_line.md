## This document shows you how to work with Git at the command line 
You need to open the Terminal window and follow the commands
---

```
%pwd # Leads to the home directory 
```
```
% cd git-github # Change directory 
%git-github % mkdir git_1 # make a subdirectory within first  
```

we have created a subdirectory /Users/mary-tziraki/git-github/git_1/

we are now in the git_1 subdirector 
We initiate it to be a git directory where we can store versions of our files.

```
(base) mary-tziraki@MBmtzirakisMBP git_1 % git init
```
Output 
```
hint: Using 'master' as the name for the initial branch. This default branch name
hint: is subject to change. To configure the initial branch name to use in all
hint: of your new repositories, which will suppress this warning, call:
hint: 
hint: 	git config --global init.defaultBranch <name>
hint: 
hint: Names commonly chosen instead of 'master' are 'main', 'trunk' and
hint: 'development'. The just-created branch can be renamed via this command:
hint: 
hint: 	git branch -m <name>
Initialized empty Git repository in /Users/mary-tziraki/git-github/git_1/.git/
```

We want now to see what is inside the directory with the ls -a command
```
% ls -a # # ensure the .git subdirectory is still present in the git_1
```
Output 
```
(base) mary-tziraki@MBmtzirakisMBP git_1 % ls -a
.	..	.git
```
the .   ..  .git indicates that the folder could be modified with git since there is the .git

Git uses this special subdirectory to store all the information about the project, including all files and sub-directories located within the project’s directory. If we ever delete the .gitsubdirectory, we will lose the project’s history.


We carry on building subdirectories and make them accesible by git 

(insert terminal window)

(show folder structure)

The main commands for that are 
```
%mkdir flowers    # make a subdirectory git_1/flowers
% cd flowers       # go into flowers subdirectory
%git init       # make the flowers subdirectory a Git repository
% ls -a          # ensure the .git subdirectory is present indicating we have created a new Git repository
```



## How to create the main brance 
Next, we will change the default branch to be called main. This might be the default branch depending on your settings and version of git. 

```
mary-tziraki@MBmtzirakisMBP flowers % cd .. ## goes up one directory which is git_1

(base) mary-tziraki@MBmtzirakisMBP git_1 % git checkout -b main
```
Output 

Switched to a new branch 'main'
(base) mary-tziraki@MBmtzirakisMBP git_1 % git status
On branch main

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)
	.DS_Store
	flowers/

nothing added to commit but untracked files present (use "git add" to track)

Its shows  the directories within git_1 (which we make main branch)

Then **nothing to commit** to do so we need to run **% git add** 


## How to Delete .git repositories in. the file

If we want to delete the .git in the flowers/.git  we go to a directory ahead (ie git_1) and we remove the .git repository

```
git_1 % rm -rf flowers/.git ## at git_1 directory remove subdirectory 
git_1 % cd flowers # 
 mary-tziraki@MBmtzirakisMBP flowers % ls -a # Look inside at flowers 

 *Output*

 .	..
 ```
 The . .. indicates that ther is not .git so tehre is not a Gir repository there.

 But be careful! Running this command in the wrong directory will remove the entire Git history of a project you might want to keep. Therefore, always check your current directory using the command pwd

 ## Tracking Changes

 Create a text file in the planet directory 

```
% nano project1.txt
```

Output 
(it opens a text editor and write…. 

Start writing the text 

 Press Ctr O to write(save) and Ctr X to exit)

If we want to see what is in the file 
```
 % cat project1.txt
 ```

Output…..is what we have written in project1.txt


If we want to check the status of the project 
```
% git status ##
```
Output 

(add picture terminal3)

The **untracked files** message means that there’s a file in the directory that Git isn’t keeping track of. We can tell Git to track a file using **git add**

```
git_1 % git add project1.txt ## Adds the text file at the stage where we will change it 

git_1 % git status# we check if the txt file is on stage


(add picture terminal4)

Git now knows that it’s supposed to keep track of project1.txt, but it hasn’t recorded these changes as a commit yet. To get it to do that, we need to run one more command:
The following command initiates the commit
```
% git commit -m "Adding second paragraph at project1.txth" 
```

(add picture terminal5)

When we run git commit, Git takes everything we have told it to save by using git add and stores a copy permanently inside the special .git directory. This permanent copy is called a commit (or revision) and its short identifier is [main (root-commit) **b52cc49**] Your commit may have another identifier.
We use the -m flag (for “message”) to record a short, descriptive, and specific comment that will help us remember later on what we did and why. If we just run git commit without the -m option, Git will launch nano (or whatever other editor we configured as core.editor) so that we can write a longer message.


Run 
```
% git status
%git lo log
```

(insert code)



OUTPUT



(base) mary-tziraki@MBmtzirakisMBP git_1 % git log
commit b52cc49efa2115999750af2124543fd278daa1aa (HEAD -> main)
Author: Mary Tziraki <m.tziraki@gmail.com>
Date:   Tue Nov 23 13:11:06 2021 +0000

 Adding second paragraph at project1.txth

 This indicates the commit **code** as **Head to main**
 The **Author**, The **date** the commit **name**

 git log lists all commits made to a repository in reverse chronological order. The listing for each commit includes the commit’s full identifier (which starts with the same characters as the short identifier printed by the git commit command earlier), the commit’s author, when it was created, and the log message Git was given when the commit was created.
--



### Where are the CHANGES we made?
#### There are not changes  yet

 The project1.txt is on stage and we are ready to make the changes

 We recall the editor "nano" and we write the extra text. We see them with %cat project1.txt
 ### Where are the CHANGES we made?

 ````
 % nano project1.txt
 ```
 Opens the editor, and we write 

 ```
 % cat project1.txt
 ```
 We see what is written

 ```
 %git status # Shows what is modified 
 ```
```
% git log # shows all the commits, authors, date 
```

 ### The terminal window

 ![Semantic description of image](/Users/mary-tziraki/git-github/terminal_7.jpg "command %git log")
 





