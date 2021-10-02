# git-101

## Beginner

### Basic commands

- init repository : `git init`
- add a file : `git add filename`
- add all files : `git add .`
- commit : `git commit -m "commit message"`
- check status which files you have added/deleted/modified : `git status`
- push code : `git push origin branch_name`

### Full Examples

#### Create a new repository

- Create a repository : Create an empty repository in [github](https://github.com/)

Then open git bash/terminal in your local pc

- init project : `git init` (initializing our repository)

For example, let's add something into our repo. Let's add a file named README.md. You can create a file using your GUI(Graphical User Interface). In FileManager, right click on mouse and file or folder creation options will be popped up. Or you can use your shell/bash terminal to create the file.

As i'm a linux user and taking flex in front of you, I will create the file using my oh-my-zsh(a bash terminal).

- create a file in bash : `touch README.md` (this will create a empty file named README.md in the directory you are in now, you can check current directory using `pwd` in terminal). You can add some content in it.

Now we have created a file and we want to add it into our repository. It does exist in our local pc not in github server yet[check if you don't believe me :)].
To upload it we need to follow some stuffs -> ['add','commit','push'].Let's do it.

- Add the file in git : `git add README.md`.

If you are curious enough and lazy :D then you must be thinking of 'adding 100 files/folder will fuck our hand and mind!'. Actually we can add all files or files with same extension or file starting or ending with same substring and so on!

- Add all files in the current dir : `git add .` (a dot can save your life :3)
- Commit changes : `git commit -m "short but meaningful commit message" -m "description can be added but its optional"`

According to my previous statement, we need to push the commit but there is a small thing we need to do as we want to connect our local repo with e github server repository we have created at first. So we need to make a link/connection for the first time. Before that we will change/move/rename the branch name. If your are in a terminal you may be notice that the default branch is master now.

![master](assets/images/bash-master.png)

In the screenshot you can see some colorful text.Forgot about the first text `(base)` its a different stuff to describe (not related to git). After (base) next things are `username@pc_name>working_directory>git_branch_name` accordingly.
We here my branch name is `master`

We will change the default branch name to `main` according to github's preference.

- rename branch : `git branch -M main`

Let me describe what we have done here. We just have changed the branch name from master to main. We could have used `git branch -m main` but there is a little differences between `-m` and `-M`. Actually `-m` define the changing but there can be a scenario where the branch name `main` already exist where we had to force git to change branch name. `-f` or `--force` is used to do something forcefully. `-M` is actually a short form of `-m -f` here. We will learn a lot about branch command later.

Now we need to link our local repo with github server somehow !

- `git remote add origin https://github.com/your_username/github_repository_name`

by this command we are creating a origin / we are adding a location of our remote repository where we will push our file or pull files from.

- push code to github : `git push origin main` (as our branch name is main)

#### Working on a repository

Scenario is we have a repository and we want to contribute in that open source project.

Link of the repository : [git-101](https://github.com/jspw/git-101)

- First of all we need to clone the repository : `git clone https://github.com/jspw/git-101.git` (this will create a folder named git-101 and copy the repository)

If we wish to copy the repo into a folder as our wish, then we can just add the folder name at the end of the command like this `git clone repo_url dir_name`

Now we have cloned the repo and we can add changes as our wish (not exactly your wish though :3).

Lets assume we have added a file named contributor.md and other files as well. Now we need to add the files or directories.

- add all files : `git add .`
- commit changes : `git commit -m 'add contributor file'`
- push code : `git push origin main` (this is a very beginner level tutorial, actually we never push code into main directly, we will lean this things later)

## Intermediate

### Some intermediate commands

- list of all branches : `git branch`
- create a new branch : `git branch branch_name`
- delete a branch : `git branch -d branch_name`
- checkout (shift from one branch to another) : `git checkout branch_name`
- create a new branch and checkout : `git checkout -b new_branch_name`

## Advance
