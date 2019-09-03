# ClassMaterial


## Git Guide 
[Git Tutorial](https://try.github.io/)

### Setting Up GitHub
#### Install git   
Installing git should be a simple `apt-get / yum/ etc install`. [reference](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git)

#### Clone remote repository 

![image](https://user-images.githubusercontent.com/18457707/64138812-85842b00-ce39-11e9-919e-d196e241db81.png)

You can get web URL for repository just as above image.

You can clone the current lab repository by issuing the following command on the command line: 

```bash
# format
$ git clone [web URL]

# example
$ git clone https://github.com/SWE3003-41/ClassMaterial.git
```

If you get an error doing clone most likely the cause is that you just haven't finished setting up your Github account.

Than change your working path to your newly cloned repository:
```bash
$ cd ClassMaterial
```

### Getting Newly Released Commit

Once new commit version is released, pull in the changes from your local directory:
```bash
$ git pull origin master
```
