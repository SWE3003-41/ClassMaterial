# ClassMaterial


## Index
- [Git Guide](https://github.com/SWE3003-41/ClassMaterial#git-guide)
- Install SQLite: [README](https://github.com/SWE3003-41/SQLite/blob/master/sqlite-source/README.md) / [pdf](https://github.com/SWE3003-41/ClassMaterial/blob/master/SQLite_installation.pdf)  
- Install and run YCSB-TS: [README](https://github.com/SWE3003-41/YCSB-TS/tree/master/jdbc/README.md) 
---


## Git Guide 

### Useful links
- [Git Tutorial](https://try.github.io/)
- [install git](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git)
- [configuring remote for a fork](https://help.github.com/en/articles/configuring-a-remote-for-a-fork)
- [syncing a fork](https://help.github.com/en/articles/syncing-a-fork)

### Setting Up GitHub
#### > Install git   
Installing git should be a simple `apt-get / yum/ etc install`.

#### > Clone remote repository 

![image](https://user-images.githubusercontent.com/18457707/64138812-85842b00-ce39-11e9-919e-d196e241db81.png)

You can get web URL for repository just as above image.

1. You can clone the current lab repository by issuing the following command on the command line: 

```bash
# format
$ git clone [web URL]

# example
$ git clone https://github.com/SWE3003-41/ClassMaterial.git
```

If you get an error doing clone most likely the cause is that you just haven't finished setting up your Github account.

2. Than change your working path to your newly cloned repository:
```bash
$ cd ClassMaterial
```

### Getting Newly Released Commit

Once new commit version is released, pull in the changes from your local directory:
```bash
$ git pull origin master
```

### Work on your own account 
#### > Fork
!! **In case of miniBase project fork repository and work on your own account!**

![image](https://user-images.githubusercontent.com/18457707/64154143-2ccd8600-ce6b-11e9-9707-fd5a9d2134bd.png)

Press `Fork` button to work on your own repository. 

![image](https://user-images.githubusercontent.com/18457707/64154282-774f0280-ce6b-11e9-8a61-122ca1a8b951.png)

Than you can see forked repository on your own account.



#### > Configuring a remote for a fork
1. Clone forked repository:
```bash
$ git clone https://github.com/[YOUR_USER_NAME]/[FORKED REPO].git
```

2. List the current configured remote repository for your fork:
```bash
$ git remote -v
  origin htts://github.com/[YOUR_USER_NAME]/[FORKED REPO].git (fetch)
  origin htts://github.com/[YOUR_USER_NAME]/[FORKED REPO].git (push)
```

3. Specify a new remote __upstream__ repository that will be synced with the fort
```bash
$ git remote add upstream https://github.com/SWE3003-41/[ORIGINAL_REPO].git
```

4. Verify the new upstream repository you've specified for your fork
```bash
$ git remote -v
  origin htts://github.com/[YOUR_USER_NAME]/[FORKED REPO].git (fetch)
  origin htts://github.com/[YOUR_USER_NAME]/[FORKED REPO].git (push)
  upstream htts://github.com/SWE3003-41/[ORIGINAL_REPO].git (fetch)
  upstream htts://github.com/SWE3003-41/[ORIGINAL_REPO].git (push)
```

#### > Syncing a fork
0. Change the current working directory to your local project
1. Fetch the branches and their respective commits from the upstream repo. Commits to master witll be stored in local brance, `upstream/master`.
```bash
$ git fetch upstream
> remote: Counting objects: 75, done.
> remote: Compressing objects: 100% (53/53), done.
> remote: Total 62 (delta 27), reused 44 (delta 9)
> Unpacking objects: 100% (62/62), done.
> From https://github.com/SWE3003-41/[ORIGINAL_REPO]
>  * [new branch]      master     -> upstream/master
```

2. Check out your fork's local `master branch`
```bash
$ git checkout master
  Swithed to branch 'master'
```

3. Merge the changes from `upstream/master` into your local `master branch`. 
```bash
$ git merge upstream/master
```
