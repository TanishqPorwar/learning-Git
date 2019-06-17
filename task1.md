# Answer

## Q1
VCS stands for  version control system. It allows you to track the history of a collection of files. It supports creating different versions of this collection.
There are many benefits of using a version control system for your projects. Some of them are:
* ### Collaboration :
  Without a VCS in place, you're probably working together in a shared folder on the same set of files. Shouting through the office that  you are currently working on file "xyz" and that, meanwhile, your teammates should keep their fingers off is not an acceptable workflow
* ### Storing Versions : 
  A VCS acknowledges that there is only one project. Therefore, there's only the one version on your disk that you're currently working on. Everything else - all the past versions and variants - are neatly packed up inside the VCS. When you need it, you can request any version at any time and you'll have a snapshot of the complete project right at hand.
* ### Restoring Previous Versions : 
  Being able to restore older versions of a file (or even the whole project) effectively means one thing: you can't mess up! If the changes you've made lately prove to be garbage, you can simply undo them in a few clicks
* ### Understanding What Happened : 
  Every time you save a new version of your project, your VCS requires you to provide a short description of what was changed. Additionally (if it's a code / text file), you can see what exactly was changed in the file's content.


## Q2
### Cloning a repository
1. On GitHub, navigate to the main page of the repository.

2. Under the repository name, click Clone or download.

  ![picture alt](https://help.github.com/assets/images/help/repository/clone-repo-clone-url-button.png)

3. In the Clone with HTTPs section, click :clipboard: to copy the clone URL for the repository

  ![picture alt](https://help.github.com/assets/images/help/repository/https-url-clone.png)
  
4. Open cmd :

5. Change the current working directory to the location where you want the cloned directory to be made.

6. Type `git clone`, and then paste the URL you copied in Step 2.
   ```
   git clone https://github.com/YOUR-USERNAME/YOUR-REPOSITORY
   ```
7. Press Enter. Your local clone will be created.


## Q3
### Pushing to a remote
Use `git push` to push commits made on your local branch to a remote repository.

The `git push` command takes two arguments:

* A *remote name*, for example, `origin`
* A *branch name*, for example, `master`
For example:
```
git push  <REMOTENAME> <BRANCHNAME>
```
As an example, you usually run `git push origin master` to push your local changes to your online repository.

### Pull
`git pull` is a convenient shortcut for completing both `git fetch` and `git merge` in the same command:
```
$ git pull remotename branchname
# Grabs online updates and merges them with your local work
```


## Q4
### Check the status of the repository
Use the `git status` command, to check the current state of the repository.

RUN:
```
git status
```
The command checks the status and reports that there’s nothing to commit, meaning the repository stores the current state of the working directory, and there are no changes to record.


## Q5
### Creating a branch
Before creating a new branch, pull the changes from upstream. Your master needs to be up to date.
```
$ git pull
````
Create the branch on your local machine and switch in this branch :
```
$ git checkout -b [name_of_your_new_branch]
```
Push the branch on github :
```
$ git push origin [name_of_your_new_branch]
```
### Switch branches
Use the checkout command to switch branch.
```
$ git checkout <branch>
```


## Q6
### git remote add
To create a new remote connection we use the ```git remote add [name] [url] command.```

The `name` is what we give to the connection. Its like a bookmark for the repository connection.

The `url` is the url of the repository that we want to connect to.


## Q7
