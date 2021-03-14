# What is Git ?
**Git is a distributed version control system**

### what does tht mean ?
* It's a system that records changes to our file overtime
* We can recall specific versions of those files at any given time
* Many people can easily collaborate on a project and have their own version of project files on their computer

## Why use git ?
* Store revisions in a project history in just one directory
* Rewind to any revision in the project I wanted to
* Work on new features without messing up the main codebase
* Easily collaborate with other programmers


## Gihub
* It is an online service that host our project
* Share our code with other developers
* Developers can share the project and work on them
* They can re-upload their edits and merge them with
the main codebase

*Note: Repository/Repo is a container or file that you want git to track your files*



## Stages that exists in our repository
### Modified/Untracked
This are files that we modified that have not been track or staged

### Staging
This are files that we track and are ready to be committed to our
repository. When ever we commit our files, only files that are in
the staging area will get committed.


### Commits
Commits are like save points or snapshots of our project, they are the particular
points in our repository that we want github to save the changes. All files that
are in the staging area get committed when we make a commit action call. Each commit
has a unique reference ID that we can reference to when we want to go back in time.

**Note: Branch is the version of our repository we are working on. The default branch
is the master branch but we might have other branches which are just the copy of our
original/master branch**

<br>
<br>



# CHEATSHEET

### Set up a configuration username and email so that github knows who
### is making the changes
~~~bash
    git config --global user.name yourUsername
    git config --global user.email urEmail@service.com    
~~~

### Logging your configuration username and email
~~~bash
    git config user.name
    git config user.email    
~~~

### Initializing a git repository: create a hidden .git file 
~~~bash
    git init
~~~

### Get the status of your repository to know which files are untracked and also on the staging area
~~~bash
    git status
~~~

### Adding a single file or a folder to the staging area 
~~~bash
    git add index.html
    git add public
~~~

### Removing a file from the staging area
~~~bash
    git rm --cached index.html
~~~

### Adding all untracked files to the staging area at once
~~~bash
    git add .
~~~

### Committing staging files
~~~bash
    git commit -m "A very descriptive message to descripe what you changed."
~~~


### Logging your repository commit history
~~~bash
    git log
~~~

### A very short version of your commit details with less information
~~~bash
    git log --oneline
~~~

## Going back in time

### Inspect a particular commit
*Go back in time to see a particular stage of your commit using the ID of that commit, it is a read only action, you can't modified anything*
~~~bash
    git checkout commitID
~~~

### Moving back to the master branch
*After you are done inspecting your code using checkout, you can go back to the master branch using*
~~~bash
    git checkout master
~~~


### Revert the changes made in a commit using its ID
*A new commit will be created that will undo all the things changes that
were made in that particular commit. But the commit will not be removed from
the commit history, we can still go back and review if we want.
~~~bash
    git revert commitID
~~~


### Reset your repository to a particular commit
*This will reset/delete every commit that happened after the commit ID we
passed to it. It will basically delete  the commits and also the commit history.
But it won't delete the changes from your repository. So you might want to recommit all the reset commit using one commit or do something with it*
~~~bash
    git reset commitID
~~~

### Hard Reset
*It is the same thing with reset but a hard one. Adding a --hard flag to the command will make it delete the commits and also the changes they made to our repository*
~~~bash
    git reset commitID --hard
~~~




