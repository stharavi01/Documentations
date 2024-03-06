## Basics

### Create a new repository on the command line

git init
git add README.md
git commit -m "first commit"
git branch -M main    //M => move or rename branch name 
git remote add origin https://github.com/stharavi01/gitTutorial.git
git push -u origin main //u => set up tracking relationship between local main branch and remote main branch on the origin repository


### Push an existing repository from the command line

git remote add origin https://github.com/stharavi01/gitTutorial.git
git branch -M main
git push -u origin main


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

### Merge Branches

git merge <branch-to-merge>


## Remote Repositories

### Pull Changes from a Remote Repository

git pull origin <branch-name>


### Push Changes to a Remote Repository

git push origin <branch-name>


### Fetch Changes from a Remote Repository (Without Merging)

git fetch origin


### View Remote Repositories

git remote -v


## Advanced Operations

### Remove a File from the Staging Area

git reset <file>


### Git Stash
git stash -u (adds untracked changes as well)

git stash save "message" (provide message to stash)


### Undoing Changes
git revert commit hash (create a new commit that undoes the changes made in a previous commit.)
git revert HEAD (undo most recent changes)
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
