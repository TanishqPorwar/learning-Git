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
### merge two branches
1. Open Git Bash.

2. Change the current working directory to your local project.

3. Check out the branch you wish to merge to. Usually, you will merge into `master`.
```
  $ git checkout master
```

4. `Pull` the desired branch from the upstream repository. This method will retain the commit history without modification.
```
  $ git pull https://github.com/ORIGINAL_OWNER/ORIGINAL_REPOSITORY.git BRANCH_NAME
```

5. Commit the merge.

6. Review the changes and ensure they are satisfactory.

7. `Push` the merge to your GitHub repository.
```
  $ git push origin master
```


## Q8
###  Resolve merge conflicts
Merge conflicts happen when you merge branches that have competing commits, and Git needs your help to decide which changes to incorporate in the final merge.

1. #### Resolving a merge conflict on GitHub
    * Under your repository name, click  Pull requests.
      
      ![picture alt](https://help.github.com/assets/images/help/repository/repo-tabs-pull-requests.png)
  
    * In the "Pull Requests" list, click the pull request with a merge conflict that you'd like to resolve.

    * Near the bottom of your pull request, click Resolve conflicts.
      
      ![picture alt](https://help.github.com/assets/images/help/pull_requests/resolve-merge-conflicts-button.png)


    * Decide if you want to keep only your branch's changes, keep only the other branch's changes, or make a brand new change, which may   incorporate changes from both branches. Delete the conflict markers <<<<<<<, =======, >>>>>>> and make the changes you want in the final merge.
      
      ![picture alt](https://help.github.com/assets/images/help/pull_requests/view-merge-conflict-with-markers.png)


    * If you have more than one merge conflict in your file, scroll down to the next set of conflict markers and repeat steps four and  five to resolve your merge conflict.

    * Once you've resolved all the conflicts in the file, click Mark as resolved.
      
      ![picture alt](https://help.github.com/assets/images/help/pull_requests/mark-as-resolved-button.png)

    * If you have more than one file with a conflict, select the next file you want to edit on the left side of the page under "conflicting files" and repeat steps four through seven until you've resolved all of your pull request's merge conflicts.
      
      ![picture alt](https://help.github.com/assets/images/help/pull_requests/resolve-merge-conflict-select-conflicting-file.png)


    * Once you've resolved all your merge conflicts, click Commit merge. This merges the entire base branch into your head branch.
      
      ![picture alt](https://help.github.com/assets/images/help/repository/https-url-clone.png)


    * If prompted, review the branch that you are committing to. If you want to commit to this branch, click I understand, update BRANCH.
      
      ![picture alt](https://help.github.com/assets/images/help/pull_requests/merge-conflict-confirmation.png)

    * To merge your pull request, click Merge pull request. 

2. #### Resolving a merge conflict using the command line
    * Open Git Bash.

    * Navigate into the local Git repository that has the merge conflict.     
    ```
      cd REPOSITORY-NAME
    ```

    * Generate a list of the files affected by the merge conflict. In this example, the file styleguide.md has a merge conflict.
    
      ```
      $ git status
      > # On branch branch-b
      > # You have unmerged paths.
      > #   (fix conflicts and run "git commit")
      > #
      > # Unmerged paths:
      > #   (use "git add ..." to mark resolution)
      > #
      > # both modified:      styleguide.md
      > #
      > no changes added to commit (use "git add" and/or "git commit -a")
      ```
      
    *  Open your favorite text editor, such as Atom, and navigate to the file that has merge conflicts.

    * To see the beginning of the merge conflict in your file, search the file for the conflict marker <<<<<<<. When you open the file in your text editor, you'll see the changes from the HEAD or base branch after the line <<<<<<< HEAD. Next, you'll see =======, which divides your changes from the changes in the other branch, followed by >>>>>>> BRANCH-NAME. 
    
    * Decide if you want to keep only your branch's changes, keep only the other branch's changes, or make a brand new change, which may incorporate changes from both branches. Delete the conflict markers <<<<<<<, =======, >>>>>>> and make the changes you want in the final merge. 
    
    * Add or stage your changes.
      ```
      $ git add
      ```.
    * Commit your changes with a comment.
      ```
      $ git commit -m "Resolved merge conflict by incorporating both suggestions."
      ```
      
## Q9
### Commit changes
* Stage your changes
  ```
  git add ~A
  ```
* Commit your changes
  ```
  git commit -m "added my github name"
  ```
 
 
## Q10
### Stash changes
* Open Git Bash.

* Navigate into the local Git repository

* stash 
  ```
  $ git stash
  ```
  
