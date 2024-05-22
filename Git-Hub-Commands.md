**Merge**
Definition: Merging is the process of integrating changes from one branch into another.
Usage: When you want to combine the changes from a feature branch into the main branch.
git checkout main
git merge feature-branch

**Rebase**
Definition: Rebasing is the process of moving or combining a sequence of commits to a new base commit. It replays commits from one branch onto another.
Usage: When you want to maintain a linear project history.
git checkout feature-branch
git rebase main

**Checkout**
Definition: Checkout is used to switch branches or restore working tree files.
Usage: When you want to switch to a different branch or restore a file from a specific commit.
git checkout branch-name
To create a new branch and switch to it:
git checkout -b new-branch

**Push**
Definition: Pushing is the process of sending your committed changes to a remote repository.
Usage: When you want to share your changes with others or update the remote repository with your local changes.
git push origin branch-name

 
**Pull**
Definition: Pulling is the process of fetching and merging changes from a remote repository to your local repository.
Usage: When you want to update your local repository with the latest changes from the remote repository.
git pull origin branch-name

 
**Cherry-pick**
Definition: Cherry-picking is the process of applying the changes from a specific commit to another branch.
Usage: When you want to apply a specific change from one branch to another without merging the entire branch.
git cherry-pick commit-hash

 
**Squash**
Definition: Squashing is the process of combining multiple commits into one.
Usage: When you want to clean up your commit history before merging a feature branch into the main branch.
git rebase -i HEAD~n
 In the interactive mode, replace 'pick' with 'squash' for the commits you want to squash

git rebase -i HEAD~3
# In the editor, change:
# pick a1b2c3 First commit
# pick d4e5f6 Second commit
# pick g7h8i9 Third commit
# To:
# pick a1b2c3 First commit
# squash d4e5f6 Second commit
# squash g7h8i9 Third commit

 
Merge: Integrates changes from one branch to another.
Rebase: Moves or combines commits to a new base.
Checkout: Switches branches or restores files.
Push: Sends local changes to a remote repository.
Pull: Fetches and merges changes from a remote repository.
Cherry-pick: Applies changes from a specific commit.
Squash: Combines multiple commits into one.
