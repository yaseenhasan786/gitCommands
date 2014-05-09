# Git Commands

Welcome! I created a simple video playlist on how to use Git & 
Github.com [here](https://www.youtube.com/playlist?list=PLPXsMt57rLtgpwFBqZq4QKxrD9Hhc_8L4&action_edit=1)

### Creating a repository online for the <b>1st time</b>!
``` sh
# navigated into your folder you want to put on Github
$ touch README.md # initialize your git repository locally
$ git init
$ git add README.md . # adds everything changed from local to staging
$ git commit -m "first commit" # commits everything in staging to be ready to be pushed to Github
$ git remote add origin https://github.com/quinnliu/GitCommands.git
$ git push -u origin master
# put in username & password
```

### When adding on to your repository online with changes
``` sh
$ git add .
$ git add -u # when you have deleted a local file you want to remove from your repo
$ git commit -m 'what has changed'
$ git push 
# put in username & password
```

### No more username & password input for every push
``` sh                      
$ git remote set-url origin git@github.com:yourUsername/yourReponame.git
```

### Working together from perspective of person that doesn't have the main repo
``` sh
# fork repo you want to work on
$ git clone https://github.com/yourUsername/yourReponame.git
# add changes to your forked repo 
# make a pull request!
$ git pull # use this after someone else has made a change to the online repo 
           # your working on and you want to make your local repo up to date
```

### Want to remove a file frome online github repo but keep it locally
```sh
$ git rm --cached localFileName
# add localFileName to .gitignore file 
# then commit these changes
# push these changes to your repo!
```

### Commands for fixing problems
```sh
# undo multiple commits  
$ git reset --hard commitSHA###...= changes staging index and local folder to match online repository commit

# removing 3 commits from online github repo
$ git push -f origin HEAD^^^:branchNameToUndoLast3Pushs
```

### Branch Commands 
```sh
$ git branch # list all branches in working folder  
$ git branch newBranchName  
$ git checkout newBranchName # switch to branch newBranchName
$ git push origin newBranchName # adds new branch to github repo
$ git branch -d branchNameToDelete # delete branch while you are on a different branch 
```