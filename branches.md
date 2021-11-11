MANAGING BRANCHES 
# Creates a new branch called bugfix
GIT BRANCH BUGFIX 
# Switches to the bugfix branch 
git checkout bugfix 
# Same as the above 
git switch bugfix 
# Creates and switches 
git switch -C bugfix 
# Deletes the bugfix branch
git branch -d bugfix 

COMPARING BRANCHES
# Lists the commits in the bugfix branch not in master 
git log master..bugfix 
# Shows the summary of changes 
git diff master..bugfix 

STASHING 
# Creates a new stash 
git stash push -m “New tax rules” 
# Lists all the stashes 
git stash list 
# Shows the given stash 
git stash show stash@{1} 
# shortcut for stash@{1} 
git stash show 1 
# Applies the given stash to the working dir 
git stash apply 1 
# Deletes the given stash 
git stash drop 1 
# Deletes all the stashes 
git stash clear 

MERGING 
# Merges the bugfix branch into the current branch 
git merge bugfix 
# Creates a merge commit even if FF is possible 
git merge --no-ff bugfix 
# Performs a squash merge 
git merge --squash bugfix 
# Aborts the merge 
git merge --abort 

VIEWING THE MERGED BRANCHES 
# Shows the merged branches 
git branch --merged 
# Shows the unmerged branches 
git branch --no-merged 

REBASING 
# Changes the base of the current branch
git rebase master 

CHERRY PICKING 
# Applies the given commit on the current branch 
git cherry-pick dad47ed 
