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

## Working Remotely using github

### Pushing to a remote repository
*In this example we assume we are pushing it to the remote master branch*
~~~bash
    git push https://github.com/path/to/repoUrl master
~~~

### Adding alias to a remote repository url
*This will make it easier for us to use the alias intead of always using the long repository url. To push code now we'll use "git push origin master" origin is the name of the alias*
~~~bash
    git remote add origin https://github.com/path/to/repoUrl
~~~


## Using Github
Github is a remote hosting service for our repository


### Description on how we collaborate on github
Let say you are working in a team and your project that you are working on is hosted on github. If you want to add a new feature to the project you are working on you'll usually use the steps below

* Create a new branch and move into it so that you can work on your new feature in an isolated branch so that you do not modify the master branch directly.

* After you are done with the new feature, you then commit the changes in that new branch.

* Push the new feature to the remote repository but NOT in the master branch of the remote repository but in a new branch usually name the same as the new branch you are working on. We do that by running the command
```bash
    git push origin new-feature
```

* The above command will create a branch named new-feature in the remote repository and then push to it. If the branch is already created, it will just push to it.

* In our github page we'll be notified that a new branch has been added to the repository and it will shows us the option to compare and then pull the new branch to the master branch.

* If we click the compare and pull option, we'll be take to a page where we can see the changes that was made, we can add comment and reviews. We can also then a merge request, this merge request will notify the developers working on that repository, they will then check the changes and send comment if they have any.

* You can then add the developers who you want to review your code.

*






