# Git Commands

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
$ git commit -m 'what has changed'
$ git push 
# put in username & password
```

### No more username & password input for every push
``` sh                      
$ git remote set-url origin git@github.com:yourUsername/yourReponame.git
```