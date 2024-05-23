# GitHub Commands Cheat Sheet

```sh
# Configure Git with your user information
git config --global user.name "Your Name"
git config --global user.email "your-email@example.com"

# Initialize a new Git repository
git init

# Clone an existing repository
git clone https://github.com/username/repository.git

# List all branches
git branch

# Create a new branch
git branch branch-name

# Switch to a branch
git checkout branch-name

# Create and switch to a new branch
git checkout -b branch-name

# Merge a branch into the current branch
git merge branch-name

# Check the status of your files
git status

# Add changes to the staging area
git add file-name

# Add all changes to the staging area
git add .

# Commit changes
git commit -m "Commit message"

# Commit with extended message
git commit
# This will open your default text editor to write a detailed commit message

# Push changes to the remote repository
git push origin branch-name

# Pull changes from the remote repository
git pull origin branch-name

# Show commit history
git log

# Show commit history with patches
git log -p

# Show a specific commit
git show commit-id

# Unstage a file
git reset HEAD file-name

# Revert changes in a file
git checkout -- file-name

# Amend the last commit
git commit --amend

# Adding a remote repository
git remote add origin https://github.com/username/repository.git

# List all configured remote repositories
git remote -v

# Remove a remote
git remote rm remote-name

# Create a new tag
git tag tag-name

# Push tags to the remote repository
git push origin tag-name

# List all tags
git tag

# Add a submodule
git submodule add https://github.com/username/repository.git

# Update all submodules
git submodule update --remote
