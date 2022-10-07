## This document shows you how to work with Git at the command line 
You need to launcg the Terminal window (ot Bash shell or git Bash in windows)  and follow the commands below:
---

## 1) Strart with Git
 Introducing yourself so git and GitHub knows who you are: 
Copy the following on your command line (terminal, bash shell) commands but not the comments that start with (#)

```
 $ git config --list # shows if you have done the initial git configurations  
```
Do you see anything? 
If not You need to tell git who you are, your email and a few settings  that would help you to follow the course.

```
$ git config --global user.name “Your Name”
$ git config --global user.email  “your_email@email.com”
$ git config --global core.editor "nano -w"
$ git config --global init.defaultBranch "main"
```

## 2)	Create the git repository and add a file.md into it


if you type **pwd** it shows wher you are 
```
%pwd # shows you the direc directory 
```
Go to any Folder (directory)  you have  by typing (ls -Fa) and then (cd YourPreferedFolder)

```
 ls -Fa
```
You see all the files and directories ( non-hiden and hiden with the . infront)
Then move to your prefered directory by 

```
 cd YourFolder 
```
and make a new directory called Project_1

```
 mkdir Project_1
```
Move into that subdirectory 


```
 cd Project_1
```
My example (not necessary the same for you, yours migh look different) 
I went from my homedirectory mary-tziraki to a subdirectory (pre-existing) called *git-github* and then I created (with mkdir) the Project_1 directory

My command line after **pwd** shows my path

```
 pwd
```
### Output
```
 /Users/mary-tziraki/git-github/Project_1
```

we have created a subdirectory with the path /Users/YOURNAME/YOUR_Pre_existing_Directory/Project_1
You are now in the Project_1 directory (folder)
### You need to make this directort a git repository
```
$ git init #  makes the folder that you are in a Git repository
```

```
 $ ls -a  # it will list all folders and files including the hiden ones (which start with . or .foldername/)
```
you will see a .git  which indicates that your directory (folder) has git and ready for version control.

**Output** 
```
.	..	.git
```


 **But be careful!** Running the git init command in the wrong directory will remove the entire Git history of a project you might want to keep. Therefore, always check your current directory using the command pwd and check if ther ie a .git directory by (ls -aF)

%pwd # shows you the path of the  directory 

If you want to create a file you type **touch** command 

```
touch README.md
```
If you want to eddit it use the **nano** editor and if you want to see it the **cat** comands

```
$ nano README.md  # Editor for the command line. Edit README.md file
```

Open in the nano editor the README.md 
Write whatever you want, for example: hellow this is a test project and Im practicing git

Then save it with (^O) and exit with (^X)

then to see the file type cat (filename)

```
$ cat README.md . # Shows the lines in the README.md file
```


## 3)	How to Stage the changes and how to commit into the repository Workflow commands
## Summary of the git commands.

```
$ git  status # Checks the branch if there are commits and shows the status
$ git add    filename1 filename2 directory/    # inserts files in the staging area
$ git  commit –m “message -what we have changed” # saves the staged content as a new commit in the local  repository
$ nano README.md  # Editor for the command line. Edit README.md file
$ cat README.md. # Shows the lines in the README.md file
```


## Add picture

You have worked (create a file, edited it and saved it) in the working directory.
TO do version control, you need to send it to the .git directory. To do so you need to add it one the STAGE area and then commit it

- **1st you checked the status** 
```
$ git  status # Checks the branch if there are commits and shows the status> You will see there if a file has beed modified (in colour) and needs to be staged and commited.
```
**Output**
```
On branch main

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)
	README.md

nothing added to commit but untracked files present (use "git add" to track)

 ```
 It says that you are in the "main" branch and you havend done any commits yet
 
The **untracked files** message means that there’s a file in the directory that Git isn’t keeping track of.
There’s a file in the directory that we have saved (modified) it in the working directory but not in git. The file is coloured !!
It tells you to use git add

We can tell Git to track the  file using **git add** then to put a 'Stamp' on it by **git  commit –m “messgae**  the commit **Dont Forget to write The Message!!!**

``
$ git add  README.md   # inserts files in the staging area, it could be many files( git add    filename1 filename2 directory/ )
$ git  commit –m “create the file and add a sentence” # saves the staged content as a new commit in the local  repository with a message

```
**Output**
```
[main (root-commit) 46961f9] create the file and add a sentence
 1 file changed, 3 insertions(+)
 create mode 100644 README.md
 ```
 
 That shows that I canged 1 file and add 3 lines (although I wrote in 2, it includes the empty lines). 
 The commit is fiven a encrypted unique number (46961f9) and has a message "create the file and add a sentence"
 
If you repeat you have the full circle of (edit, save, view, check status, add to stage and finaly commit).

It is recomended to do another git status to check!

$ git  status # Checks the branch if there are commits and shows the status> You will see there if a file has beed modified (in colour) and needs to be staged and commited.
```
**Output**
```
On branch main
nothing to commit, working tree clean
```
It says that there is nothing to commit, so everything is in the git repository and it is commited! 

### REPEAT the following workflow to practise !! Make changes and commits  

```
nano README.md
```
```
cat README.md
```
```
$ git  status
```
```
git add  README.md
```
```
$ git  commit –m “message”
```
If you are doing it continusly you will create lots of changes with the relevant commits. A picture with my workflow
## ADD Pictures






## 4)	How to see history and differences between versions:

A quick summary of the commands to use to observe the history and the differences between the files
### Summary of the commands 

- $ **git log**  # Displays ALL the information about the commits and the commit’s history 
- $ **git log --oneline**    # Displays only the essential information of the history and commits 
- $  **git diff HEAD~1 File.txt**# Displays the difference between the last commit HEAD and the commit before that HEAD~1
- $  **git checkout HEAD~1 File.txt**# Displays the difference between the last commit HEAD and the commit before that HEAD~1
- $  **git checkout f23bs45e File.txt**# Displays the difference between the last commit HEAD and the commit before that with the code (f23bs45e) You can find the codes of each commit if you type git log --oneline

### Demonstration 
```
git log # Displays ALL the information about the commits and the commit’s history 
```
## Add picture 

```
git log --oneline # Displays ALL the information about the commits and the commit’s history 
```
Everything is consize here and displays all the commits with. their messages and their unique number
HEAD is always the latest commit!!
HEAD ~ 1 :Is the previous version (it is like HEAD minus 1) commit and file!

To see the difference in the two latest versions  we use **git diff HEAD~1 README.md** 

```
git diff HEAD~1 README.md 
```
**Output**
```
diff --git a/README.md b/README.md
index 0251c25..e9566e8 100644
--- a/README.md
+++ b/README.md
@@ -2,6 +2,6 @@ Hello
 
 I've started a project with git.
 
-I need to demonstrate  that I'm doing version control!
+I need to demonstrate and write in a file called git_command_line.md that I'm doing version control!
 

```
It shows that I have subtract one line (-) and I have added another one (+) althought I have changed few words it takes it as a whole line.If I want to see the changes in various stages I use the HEAD~2 (for two versions below) and the HEAD~3 (for three versions below).

## Add picture 



## 5)	How to see the file's previous versions:


If we want to go back in versions and time We use the  **git checkout HEAD~1 File.txt**# !! the one with  HEAD~1. Another ways is    **git checkout f23bs45e File.txt**# which goes to one version bellow with the unique number. You can find the codes of each commit if you type git log --oneline.


```
git diff HEAD~1 README.md 
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
 





