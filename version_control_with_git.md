# Version Control with Git 
##	What is version control and why we use it:
Version control is the lab notebook of the digital world: it’s what professionals use to keep track of what they’ve done and collaborate with other people. Every large software development project relies on it, and most programmers use it for their small jobs as well. And it isn’t just for software: books, papers, small data sets, and anything that changes over time or needs to be shared can and should be stored in a version control system.

Version control is better than mailing files back and forth:
•	Nothing committed to version control is ever lost unless you work really hard at it. Since all old versions of files are saved, it’s always possible to go back in time to see exactly who wrote what on a particular day or what version of a program was used to generate a particular set of results.
•	As we have this record of who made what changes when, we know who to ask if we have questions later onand, if needed, revert to a previous version, much like the “undo” feature in an editor.
•	When several people collaborate on the same project, it’s possible to overlook or overwrite someone’s changes accidentally. The version control system automatically notifies users whenever there’s a conflict between one person’s work and another’s.
Teams are not the only ones to benefit from version control: lone researchers can benefit immensely. Keeping a record of what was changed, when, and why is extremely useful for all researchers if they ever need to return to the project later (e.g., a year later, when memory has faded).
Version control systems start with a base version of the document and then record changes you make each step of the way. You can think of it as a recording of your progress: you can rewind to start at the base document and playback each change you made, eventually arriving at your more recent version.

Once you think of changes as separate from the document itself, you can then think about “playing back” different sets of changes on the base document, ultimately resulting in other versions of that document. For example, two users can make independent sets of changes on the same document

Unless multiple users make changes to the same section of the document - a conflict - you can incorporate two sets of changes into the same base document.

A **version control system  (VCS)** is a tool that keeps track of these changes for us, effectively creating different versions of our files. It allows us to decide which changes will be made to the next version (each record of these changes is called **a commit**), and keeps valuable metadata about them. The complete history of commits for a particular project and their metadata make up a **repository**. Repositories can be controlled in sync across different computers, facilitating collaboration among other people.


## Git a version control system
Git is an excellent platform to manage code, it allows you to save drafts that you can look back all the previous versions, review and make changes or undo complicated errors.

A repository in Git is a project in a "Folder" that helps to manage all the project lines.

A repository contains all of the files and folders associated with your project. It also includes the revision history of each file. The file history is a series of snapshots in time, known as commits. A commit tells Git that you made some changes that you want to record.

When you make a commit in Git you will see “commit to main.” This refers to the default branch, which can be thought of as the production-ready version of your project.


There are various ways to interact with Git 
The most common one is the command line.
Some people get intimidated by Git at first site because they think it would look like an extended incomprehensive code. 

Today easy-to use interfaces make it easy to interact with Git without using the command line.
The interface used to work with is called GitHub Desktop.

For educational purposes, we will demonstrate how to work with git both ways. 
1)	Using the command line 
2)	Using the GitHub Desktop interface 
