# Git Commands - Task 

## git init
This command is used to create an empty git repository or to initialize and existing repository.

    git init

## git add
This command is used to add the files or folders into the staging area.

**To add a file to staging area:**

    git add <filename>

**To add all files or folders in the currect directory**

    git add .

## git status
This command is used to view the status of the repository and the files or folders that are present in the staging area.
This show the list of files that are tracked and untracked.


    git status 
    
**To just view the list of files that are changed**

    git status --short
    

## git config
This command is used to configure the username and email of the person working on the local repository.

**To configure username**

    git config --global user.name = <name>

**To configure email**

    git config --global user.email = <email>

## git commit

This command is used to commit the changes that are made. Commit will fetch the changes available in the staging area.
Commit command will create a snapshot of the repository.
Each and every commit will have a commit message and a commit-id. Commit message is given by the user and commit-id is generate using SHA algorithm.

    git commit -m <commit-message>
    
**To add and commit at once**
    
    git commit -a


## git log

This command is used to get the total history of the repository.
It provides the list of all the commits and for each commit it provides the username, date of commit, commit title and commit-hash.

    git log 

**To get each commit details in oneline**

    git log --oneline
    
**To get the list of files modified and no. of lines modified in each commit**

    git log --stat

**To get the list of files modified and also the location of the lines removed of added in the file**
    
    git log --patch

**To get the graph of the commits made**
Each node of graph represents a commit

    git log --graph
    
    -------------------------
    
    git log --graph --oneline

**To view last 'n' (n is a number) commit details**

    git log -n

## git diff
This command is used to view the difference between the files in the one commit and another commit.

**To view the changed before adding files to staging area**
    
    git diff

**To view the change between two different commits**

    git diff <commit1-hashkey> <commit2-hashkey>
    
**To view the change between two different branches**

    git diff <branch1-name> <branch2-name>


## git branch

This command is used for creating a new branch. In git branch are used for independent development of any particular feature. The default branch in git is master branch. Any number of branches can be made from master branch or any other branch.

**To create a new branch**
    
    git branch <branch-name>
    
**To list the existing branch names**

    git branch
    
**To delete a local branch**
The branch gets deleted only if it is merged:

    git branch -d <branch-name>

The branch gets deleted even if it not merged:

    git branch -D <branch-name>

**To restore the deleted branch**
    
    git checkout -b <branch_name> <hashkey>

## git checkout

This command is used to switch from one branch to another branch.

    git checkout <branch-name>

## git merge 
This command is used to merge the another branch with the current branch. The code present in the current branch and merged branch will be merged.

    git merge <branch-name>

## git remote
This command is used add the URLs of the remote repositories.

    git remote add <remote-url-name> <url of remote repo>
    
    Ex: git remote add origin https://github.com/Hemanthghs/gRPC-Protobuf-with-Golang.git
    
    

## git push
This command is used to push a specific branch from the local repository to the remote repository

**To push the local changes to remote repo**

    git push <remote-url-name> <branch-name>
    
    Ex: git push origin main

**To list the remote URLs**

    git remote -v 

**To edit the existing remote url**

    git remote set-url <remote-url-name> <new url>
    
## git fetch
This command will download the changes from the remote repository to the local repository. This will get the updates that are made to the remote repository into the local repository. This will only download the change and does not merge the changes.

**To fetch a remote repo**

    git fetch <remote-url>

**To fetch a specific remote branch**

    git fetch <remote-url> <branch-name>
    
**To fetch all branches**

    git fetch -all
    

## git pull
This command is combination of git fetch and git merge commands.
This command will download the changes from the remote repository to the local repo and will merge the change with the local branch. There is a chances for merge conflicts.

    git pull


## git stash



