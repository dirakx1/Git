# Git



### Workflow ###

On your repository (remote origin) you can do whatever you want and even work on your separate branches. After finishing up, 
you must consolidate all of your changes into your master branch.

After that, you must make a pull request on Github. Your work will be reviewed and then rebased into master branch, 
which then will be ready to be deployed on production.

To get the master branch from your local fork:

```
        $ git pull origin master
```

To get the master branch from the official zinadev/zina:

```
        $ git fetch upstream
        $ git rebase upstream/master
```

Your git config file (found on the project root, under ".git/config") must be like below - just change "user" to your Github's account name:

```
[core]
    repositoryformatversion = 0
    fileMode = false
    bare = false
    logallrefupdates = true
[remote "origin"]
    url = https://github.com/user/project.git
    fetch = +refs/heads/*:refs/remotes/origin/*
[branch "master"]
    remote = origin
    merge = refs/heads/master
[remote "zina"]
    url = https://github.com/group/project.git
    fetch = +refs/heads/*:refs/remotes/project/*
```

## git branching

* git checkout -b new_name
* git push origin new_name

## Branching strategies. 

* Fast-forward merge
* Qa / dev / feture / prod
* Tagging 

## Git flow 
* git flow package to set branching, releases etc

### Referencies ###
* http://robots.thoughtbot.com/keeping-a-github-fork-updated

