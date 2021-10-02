# git-101

## Beginner

### Basic commands

- init repository : `git init`
- add a file : `git add filename`
- add all files : `git add .`
- commit : `git commit -m "commit message"`
- check status which files you have added/deleted/modified : `git status`
- list of all branches : `git branch`
- create a new branch : `git branch branch_name`
- delete a branch : `git branch -d branch_name`
- checkout (shift from one branch to another) : `git checkout branch_name`
- create a new branch and checkout : `git checkout -b new_branch_name`
- push code : `git push origin branch_name`

### Full Examples

#### Create a new repository

- Create a repository : Create a empty repository in github.

Then open git bash in your local pc

- init project : `git init` (initializing our repository)

For example lets add something in our repo. Let's add a file called readme.md. You can create a file using your GUI(Graphical user interface) like in FileManager, right click on mouse and file or folder creation options will be popped up. Or you can use your shell/bash to create the file.

    As i'm a linux user and taking flex in front of you, i will create md file using my oh-my-zsh(a bash terminal).

- create a file in bash : `touch README.md` (this will create a empty file named README.md in the directory you are in now, you can check current directory using `pwd` in terminal). You can add some content in it.

Now we have created a file and we want to add it into our repository. It does exist in our local pc not in github server [check if you don't believe me :)].
To upload it we need to follow some stuffs -> ['add','commit','push'].Let's do it.

- Add a file in repo : `git add README.md`.

If you are curious enough and lazy :D then you must be thinking of adding 100 files/folder will fuck our hand and mind ! Actually we can add all files or files with same extension or file starting or ending with same substring and so on!

- Add add files in the current dir : `git add .` (a dot actually can save your life :3)
- Commit changes : `git commit -m "short but meaningful commit message" -m "description can be added but its optional"`

According to my previous statement we need to push the commit but there is a small thing we need to do as this is repo we want to connect with e github server repository we have created at first. So we need to make a link for the first time. Before that we will change/move/rename the branch name. If your are in a terminal you may be notice that the default branch is master now.

![master](assets/images/bash-master.png)

In the screenshot you can see some colorful text.Forgot about the first text `(base)` its a different stuff to describe (not related to git). After (base) next things are my `username@pc_name>working_directory>git_branch_name` accordingly.
We here my branch name is `master`

We will change the default branch name to `main` according to github's preference.

- rename branch : `git branch -M main` (we will learn more about branch command later)

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

## Advance
