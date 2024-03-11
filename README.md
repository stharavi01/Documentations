## Basics

### Create a new repository on the command line

git init </br>
git add README.md </br>
git commit -m "first commit" </br>
git branch -M main    //M => move or rename branch name  </br>
git remote add origin https://github.com/stharavi01/gitTutorial.git </br>
git push -u origin main //u => set up tracking relationship between local main branch and remote main branch on the origin repository


### Push an existing repository from the command line

git remote add origin https://github.com/stharavi01/gitTutorial.git </br>
git branch -M main </br>
git push -u origin main </br>


### Clone a Repository

git clone <repository-url>


### Stage Changes

git add <file>


### Commit Changes

git commit -m "Your commit message"


### Check Repository Status

git status // shows the staging area ie status of the repository


### View Commit History

git log  // commit hash, author,date, and commit message
// press q and enter to exit from logs


### Temporarily saving the changes and can reapply them later


git stash (it saves the staged changes but will ignore unstaged files)

git stash apply (you can apply the stashed changes to multiple branches )


## Branching

### Create a New Branch

git branch <branch-name>


### Switch to a Branch

git checkout <branch-name>


### Create and Switch to a New Branch

git checkout -b <new-branch-name>


### Delete a branch
git branch -d <branch-name> // use -D if you want to delete even when not merged

### Merge Branches

git merge <branch-to-merge>


## Remote Repositories

### Pull Changes from a Remote Repository

git pull origin <branch-name>


### Push Changes to a Remote Repository

git push origin <branch-name>


### Fetch Changes from a Remote Repository (Without Merging)

git fetch origin
git merge / git rebase


### View Remote Repositories

git remote -v


## Advanced Operations

### Rebase ( integrating changes from one branch onto another preserving the commits. )
//For example, consider a situation where the main branch has progressed since you started working on a feature branch. You want to get the latest updates to the main branch in your feature branch, but you want to keep your branch's history clean so it appears as if you've been working off the latest main branch. This gives the later benefit of a clean merge of your feature branch back into the main branch.

The primary purpose of git rebase is to maintain a cleaner and more linear commit history compared to other history-altering commands like git merge

### Merge directly or rebase and then merge

git rebase <base-branch> (<base-branch> is the branch you want to rebase onto.)

Let's say you have a feature branch feature_branch with several commits, and you want to rebase it onto the main branch:
# Assuming you are on the feature_branch
git checkout feature_branch

# Rebasing onto the main branch
git rebase main


### Remove a File from the Staging Area

git reset <file>

### merge and rebase 

git checkout your_branch  //Checkout the branch you want to update: </br>
git merge --rebase main  //Merge changes from another branch (main) using rebase: </br>
git add <conflicted_file>  //Resolve conflicts if they occur during the rebase: </br>
git rebase --continue  </br>
git commit -m "Merge changes from main using rebase" // Complete the merge-rebase: </br>
git push origin your_branch //Push the changes to the remote repository: </br>



### Git Stash
git stash -u (adds untracked changes as well)

git stash save "message" (provide message to stash)


### Undoing Changes
git revert commit hash (create a new commit that undoes the changes made in a previous commit.)</br>
git revert HEAD (undo most recent changes)</br>
git add . </br>
git commit -m "sucessfully reverted" </br>
git push origin main </br>

git revert --continue
git revert --abort

### Discard Changes in a File

git checkout -- <file> (move the head and branch ref pointer to a specified commit)


### Resolve Merge Conflicts

git merge <branch-name>
# After resolving conflicts, use 'git add' and 'git merge --continue'


### Create a Tag for a Specific Commit

git tag <tag-name> <commit-hash>


### Show Differences Between Commits, Branches, or Files

git diff <source> <destination>


## Ignore Files

### Create a .gitignore File
Add filenames or patterns to exclude them from version control.

## Miscellaneous

### Show Help and List of Commands

git --help
