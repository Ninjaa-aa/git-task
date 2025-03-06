# Project OMG - Git Workflow Documentation

This README documents the complete Git workflow established for Project OMG, our revolutionary cloud-based application. Follow these procedures to maintain proper version control and ensure smooth collaboration between team members.

## Table of Contents
1. [Repository Setup](#repository-setup)
2. [Documentation Updates](#documentation-updates)
3. [Feature Development Workflow](#feature-development-workflow)
4. [Merging Features](#merging-features)
5. [Branch Management](#branch-management)
6. [Release Tagging](#release-tagging)

## Repository Setup

Initialize a new Git repository and push the initial codebase:

```bash
# Initialize a new Git repository in the project directory
git init

# Add all project files to staging
git add .

# Create the initial commit with a descriptive message
git commit -m "Initial commit: Project OMG codebase"

# Add the remote repository URL
git remote add origin https://github.com/Ninjaa-aa/git-task.git

# Push the initial codebase to the master branch
git push -u origin main
```

## Documentation Updates

Update the documentation directly on the master branch:

```bash
# Edit the documentation file
# (Make necessary changes to doc.txt)

# Stage the modified file
git add doc.txt

# Commit the changes with a descriptive message
git commit -m "Update product documentation with latest specifications"

# Push the changes to the remote repository
git push origin main
```

## Feature Development Workflow

Create a separate branch for new feature development:

```bash
# Create and checkout a new feature branch
git checkout -b b1

# Create a new file for the feature
touch file2.txt

# Add content to the new file
# (Edit file2.txt with the necessary code/content)

# Stage the new file
git add file2.txt

# Commit the new feature
git commit -m "Add groundbreaking feature in file2.txt"

# Push the feature branch to the remote repository
git push -u origin b1
```

## Merging Features

Merge the completed feature into the master branch:

```bash
# Switch back to the master branch
git checkout master

# Merge the feature branch into master
git merge b1

# If conflicts occur, resolve them:
# 1. Open the conflicted files in your editor
# 2. Look for conflict markers (<<<<<<, =======, >>>>>>>)
# 3. Edit the files to resolve conflicts
# 4. Save the files
# 5. Stage the resolved file
git add <conflicted-files>

# Complete the merge with a commit
git commit -m "Merge feature branch b1 into master"

# Push the merged changes to the remote repository
git push origin master
```

## Branch Management

Clean up completed feature branches:

```bash
# Delete the feature branch locally
git branch -d b1

# Delete the feature branch from the remote repository
git push origin --delete b1
```

## Release Tagging

Tag stable versions for release management:

```bash
# Create a local tag for the stable version
git tag -a v1.0 -m "First stable release of Project OMG"

# Push the tag to the remote repository
git push origin v1.0
```

If a tag needs to be removed:

```bash
# Delete the tag locally
git tag -d v1.0

# Delete the tag from the remote repository
git push origin --delete v1.0
```

## Best Practices

1. **Commit Messages**: Write clear, descriptive commit messages that explain what changes were made and why.
2. **Branch Naming**: Use descriptive branch names that reflect the feature or fix being implemented.
3. **Regular Commits**: Make small, frequent commits rather than large, infrequent ones.
4. **Pull Before Push**: Always pull changes from the remote repository before pushing to avoid conflicts.
5. **Code Review**: Have team members review code before merging feature branches into master.

---

*This Git workflow documentation was created by the Emumba development team for Project OMG. For questions or clarifications, contact the project lead.*