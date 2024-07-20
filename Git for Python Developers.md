---
marp: true
theme: gaia
paginate: true
---

# Git for Python Developers
## Trainer Name: Shaounak Nasikkar

---

## What is Git?

- A version control system (VCS)
- Tracks changes in computer files and folders
- Allows collaboration on projects
- Enables reverting to previous versions

---

## Why Use Git?

**Track Changes**: See how your code evolved over time
**Collaboration**: Work with others seamlessly
**Backup**: Restore files in case of mistakes
**Versioning**: Experiment without fear of breaking things
**Secure**: Secure the code.

---

## Git Workflow

**Clone**: Download a copy of a remote repository
**Modify**: Make changes to your local files
**Stage**: Add changes you want to track in the next commit
**Commit**: Create a snapshot of your changes with a message
**Push**: Upload your commits to the remote repository (optional)
**Pull**: Download changes from the remote repository (optional)

---

## Basic Git Commands

`git clone https://github.com/git-guides/git-clone`: Downloads a repository
`git pull`: Fetches and merges changes from the remote repository
`git log`: Shows a history of commits
`git status`: Shows the current state of your working directory

---

## Staging and Committing

`git add [filename]`: Adds a specific file to the staging area
`git add .`: Adds all modified files to the staging area
`git commit -m "Your commit message"`: Creates a commit with a message

---

## Pushing and Pulling

`git push origin main`: Uploads your commits to the "main" branch on the remote repository named "origin" (replace "main" with the actual branch name)
`git pull origin main`: Downloads changes from the "main" branch on the remote repository named "origin" and merges them into your local branch

---

## Undoing Changes
`git checkout .`: Discards uncommitted changes in the working directory
`git stash`: Temporarily stores uncommitted changes
`git stash pop`: Applies the most recent stashed changes

---

## Branching and Merging

`git branch [branch-name]`: Creates a new branch
`git checkout [branch-name]`: Switches to a different branch
`git merge [branch-name]`: Merges changes from one branch into another

---

## Resources

https://git-scm.com/
https://www.atlassian.com/git/tutorials
https://ohmygit.org/

---

## Conclusion

Git is a powerful tool for managing code changes
Learning the basics will improve your development workflow
Practice makes perfect!
