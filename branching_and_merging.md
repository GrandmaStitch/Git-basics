# Branching and merging

- ### view all tags

  `git tag`

- ### add a marker on the most recent commit

  `git tag -a v1.0`

- ### delete a marker from a specific commit

  `git tag -d v1.0`

- ### add a marker on a past specific commit

  `git tag -a tagname <past-commit-id>`

- ### list out all the branch names in reposity

  `git branch`

- ### create a new branch
  
  `git branch <branch-name>`

- ### create a new branch and have it point to the commit with SHA

  `git branch <branch-name> <commit-id>`

- ### delect a branch
  
  can't delete a branch if it has commits on it that aren't on any other branch
  
  can't delete a branch that you're currently on

  `git branch -d <branch-name>`

- ### to force delection

  `git branch -D <branch-name>`

- ### switch branch
  
  this will remove all of the files that are referenced by commits in the master branch. It will replace them with the files that are referenced by the commits in the sidebar branch

  `git checkout <branch-name>`

- ### switch and create a new branch points to the specific commit id

  `git checkout -b <new-branch-name> <commit-id>`

- ### switch and create a new branch points to master branch

  `git checkout -b <new-branch-name> master`

- ### merge - combine branches together
  
  Remember that making a merge makes a commit
  
  When we merge, we're merging some other branch into the current (checked-out) branch. We're not merging two branches into a new branch. We're not merging the current branch into the other branch.

  There are two types of merges: fast-forward merge and regular type of merge.
    - fast-forward merge - the branch being merged in must be ahead of the checked out branch
    - regular type of merge - a)two divergent branches are combined b)a merge commit is created
  combine Git branches

  `git merge <name-of-branch-to-merge-in>`

- ### merge conflict - a merge fails
  
  A merge conflict happens when the same line or lines have been changed on different branches that are being merged. Git will pause mid-merge telling you that there is a conflict and will tell you in what file or files the conflict occurred. to resolve the conflict in a file:
  - locate and remove all lines with merge conflict indicators
  - determine what to keep
  - save the file(s)
  - stage the file(s)
  - make a commit