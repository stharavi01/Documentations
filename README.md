#!/bin/bash

# Define the README content
readme_content="# Git Commands Reference

This is a reference guide for common Git commands. Organized from most used to least used.

## Basics

### Initialize a Repository
\`\`\`bash
git init
\`\`\`

### Clone a Repository
\`\`\`bash
git clone <repository-url>
\`\`\`

### Check Repository Status
\`\`\`bash
git status
\`\`\`

### Stage Changes
\`\`\`bash
git add <file>
\`\`\`

### Commit Changes
\`\`\`bash
git commit -m \"Your commit message\"
\`\`\`

### View Commit History
\`\`\`bash
git log
\`\`\`

## Branching

### Create a New Branch
\`\`\`bash
git branch <branch-name>
\`\`\`

### Switch to a Branch
\`\`\`bash
git checkout <branch-name>
# or, using git switch (if Git version is 2.23 or later)
git switch <branch-name>
\`\`\`

### Create and Switch to a New Branch
\`\`\`bash
git checkout -b <new-branch-name>
# or, using git switch (if Git version is 2.23 or later)
git switch -c <new-branch-name>
\`\`\`

### Merge Branches
\`\`\`bash
git merge <branch-to-merge>
\`\`\`

## Remote Repositories

### Pull Changes from a Remote Repository
\`\`\`bash
git pull origin <branch-name>
\`\`\`

### Push Changes to a Remote Repository
\`\`\`bash
git push origin <branch-name>
\`\`\`

### Fetch Changes from a Remote Repository (Without Merging)
\`\`\`bash
git fetch origin
\`\`\`

### View Remote Repositories
\`\`\`bash
git remote -v
\`\`\`

## Advanced Operations

### Remove a File from the Staging Area
\`\`\`bash
git reset <file>
\`\`\`

### Discard Changes in a File
\`\`\`bash
git checkout -- <file>
\`\`\`

### Resolve Merge Conflicts
\`\`\`bash
git merge <branch-name>
# After resolving conflicts, use 'git add' and 'git merge --continue'
\`\`\`

### Create a Tag for a Specific Commit
\`\`\`bash
git tag <tag-name> <commit-hash>
\`\`\`

### Show Differences Between Commits, Branches, or Files
\`\`\`bash
git diff <source> <destination>
\`\`\`

## Ignore Files

### Create a .gitignore File
Add filenames or patterns to exclude them from version control.

## Miscellaneous

### Show Help and List of Commands
\`\`\`bash
git --help
\`\`\`

This is not an exhaustive list, and there are many more Git commands and options available. Refer to the official Git documentation for a complete reference.
"

# Write the content to README.md
echo "$readme_content" > README.md

# Notify the user
echo "README.md file created successfully!"
