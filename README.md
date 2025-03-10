# git-branching-
Git Branching and Tagging Workflow

Repository Setup

Clone the repository from GitHub:

git clone https://github.com/DevOps-Siba/git-branching-
cd git-branching-

Branch Management

Check available branches:

git branch

Pull the latest changes:

git pull

Switch to a new branch:

git checkout branch-1

Verify the current branch:

git branch

File Creation and Commit

Create a new file:

touch file1

Check the file status:

git status

Add and commit changes:

git add .
git commit -m "branchfile"

View commit logs:

git log

Push Changes to Remote

Push changes to the main branch:

git push origin main

Push changes to a feature branch:

git push origin branch-1

Delete a Branch

Delete a branch locally and remotely:

git branch -D branch-1
git push origin --delete branch-1

Tagging Versions

Create and push tags:

git tag v1.1.0
git push origin v1.1.0

List all tags:

git tag --list

Show tag details:

git show v1.1.0

Push all tags to remote:

git push origin main --tags

Create new tags and push:

git tag v2.1.0
git push origin main --tags

git tag v3.1.0
git push origin main --tags

Summary

This workflow demonstrates how to:

Clone a repository

Manage branches

Create and commit files

Push changes

Tag releases for version control

Use this guide as a reference for working with Git in your DevOps workflow!
