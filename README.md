# Josh-Corp

Josh Corp’s Code is maintained on Github, and we use git to maintain source control between developers in the project. This means two people can work simultaneously on the same project without interfering with the main application until approved.
# Github
Github is a service that hosts git repositories, our projects application source code can be downloaded and used by everyone, so they know what they’re running. 

## Step one cloning: 
Cloning a repo is the process of downloading the entire project so you have a copy to work and build from on your computer.
```
git@github.com:hackerpreneur/Josh-Corp.git
```
 
## Step two Creating branches:
Branches are separate versions of the source code usually maintained by other developers so new features or optimised can be implemented without affected the “main” branch. 
To create a new branch locally and move to it:
```
# Create a new branch
git branch my_branch 
# go to that new branch 
git checkout -b my_branch
``` 
 
## Step three Committing changes
Now that you have cloned your git and you have created a branch, you can make and track changes without interfering with the main branch. The first step in this is to commit any changes you make. E.g. (edit a text file, or add a new file)
Committing a new file to the repo:
```
# Create a new file
touch newfile.txt
# add that file to the git repo
git add newfile.txt
# commit the file to the repo
git commit -m git commit -m “made a new file”
```
Adding the file is the process of making sure this file or any changes are now tracked so other users can download it when they clone your branch. 
Committing is so any added files or changes are logged usually with a commit message (e.g. git commit -m “made a new file”)
Note: commits should usually be small incremental changes.

## Step four pushing those changes.
Every change and commit we’ve made thus far are local changes. But when you push your changes, they are sent to the remote Github server, where others in your project can see and download to their local repos.
```
git push origin my_branch
```
This specific command will make a remote branch called “my_branch” on the Github server. This will be separate from the main branch in which everyone starts from. 
To add any of your changes to the main branch, you usually do this via the Github website when you make a “pull request”


---

# Additional commands
Aside from the above commands which are usually used when making small incremental changes. There are commands that are used when trying to manage and merge different branches. This is common when you’re working in large teams with multiple branches.
These commands will suggest ways in which you can add those changes and merge branches. 

## git fetch
Git fetch is the command use to retrieve all the branches from a remote git repo.
```
Git fetch
```
This is useful for identifying if the branch you may be working off has changed. (e.g main) Those changes will need to be incorporated so your branch is up to date.

## git pull
Git pull will pull all the commits that were made on the remote branch and add them to your local. The local will now be a “local merge” which means it will slightly differ from the main and have your changes. 
Note: some conflicts may appear if any of the commits you pulled from the branch were edited by your local branch.
```
Git pull
```
You could also run pull with the –rebase parameter and in stead of merge directly. It will add your changes on top of the remote branches changes so its as if you are working of the latest code.
```
Git pull --rebase
```
 
## Merging
Merging is the process of combining two branches manually so you can pick and choose which changes from each you want to combine. 
```
# switch receiving branch, in this case main
Git checkout main 
# merge from sending branch
Git merge my_branch
```

