---
title: Git Fundamentals
nav\_order: 5
---

## Table Of Contents

**Configuring Git**

**Initializing a Repo**

**Staging and Commit Files**

**Status, Log, and Diff**

**Using a Git Ignore File**


# Configuring Git



You should tell Git who you are. Use these commands to configure this properly



git config --global user.name "Your Name"

git config --global user.email "your.email@example.com"



You should also turn on helpful colourization.



git config --global color.ui auto



You only need to set these once and then you're good to go!



# Initializing a Repository



To bring a new project under control we must first initialize the repository (the repo) from within the project's root folder:



To initialize a new git repo from the command prompt use this command:



git init .



Git defaults to using the word "master" (as in "master copy" or "master recording") for the main branch, but we can change this with this command:



git branch -m main



\#Staging and Committing Files



As we make changes to our code we commit the changes to our git repo.



Before we can commit we must add new or changed files to a staging area.



Here's how to stage a file:



git add filename.extention



We could also use a period to stage all new or modified files:



git add .



Wilcards and sub-folders work too:



git add docs/textfiles/*.txt



We commit our staged changes with a commit message:



git commit -m "Your explanation of the changes goes here."



For complex changes, we can include a short title, followed by a long explanation:



git commit -m "Title" -m "Long description goes here ..........";



We can even configure git to open a text editor of our choice using:



git commit



Good Commit Messages are Crucial!



Quality commit messages contribution to:

* Traceability: Commit messages clarify code history and aid in debugging.
* Collaboration: They help others understand the intentions behind changes.
* Documentation: They act as a form of source code documentation.
* Change Management: - "Change Logs" based on commits are often shipped with each release.



Bad Commit Messages:



fixing stuff



Final version.



asdf



Good Commit Messages:



Enhance user experience by validating signup form fields.



Improve code readability by refactoring PlayerRegistrationService.



Prevent null reference crashes by adding pointer checks in the teleport code.



See Conventional Commits for a lightweight commit message convention.



\#Git Status, Log and Diff



Commits can be reviewed by using:



git log



Each entry in the log shows:

* The commit hash.
* Who made the commit.
* When it was made.
* The commit message.



To compare the differences between the current files and the last commit use:



git diff



We can diff specific files:



git diff secret\_plans.txt



Or specific folders (and their sub-folders):



git diff ./textfiles/plans



To check the status of the repo for changes or additions use:



git status



This shows you all of your modified files 



\#The Git Ignore File



Sometimes there are files you don't want to include in your repo:

* Files that include secrets like passwords or API keys.
* Temporary files and folders.
* Build files and folders.
* Hidden OS files like .DS\_Store (Mac) or Thumbs.db (Windows) files.



Exclude files and folders by create a .gitignore file in the project root:



Ignore specific files.



Thumbs.db


Wildcards: Ignore all .exe files.



*.exe



Exception to wildcards: Do track the special.exe file.



!special.a



Ignore all files in any folder called build.



build/



Ignore all .pdf files in the doc/ folder and any of its sub-folders.



doc/**/*.pdf

