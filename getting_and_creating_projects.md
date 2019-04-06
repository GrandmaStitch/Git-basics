# Getting and creating projects

- ### create an empty Git repository
  the hidden .git directory is the brain/storage center for the repository. It holds all of the configuration files and directories and is where all of the commits are stored.

  `git init`

- ### create an identical copy of an existing repository

  `git clone <url>`

- ### clone a repo and give it a new name

  `git clone <url> newname`
  
- ### display the current status of the repository  
  
  `git status`

- ### display all of the commits of a repository
  
  `git log`

  - #### the --oneline flag is used to alter how git log displays information

    `git log --oneline`

  - #### the --stat flag is used to alter how git log displays information

    `git log --stat`

  - #### display the actual changes made to a file

    `git log -p or git log --patch`

  - #### to ignore changes to whitespace
  
    `git log -w`

  - #### just display a specific commit's details

    `git log -p <commitID>`

  - #### the --graph flag adds the bullets and lines to the leftmost part of the output; the --all flag is what display all of the branches in the repository

    `git log --oneline --graph --all`
    
  - #### filter by author
    
    `git log --author="<author-name>"`
    
  - #### filter commits with the --grep flag

    `git log --grep="<word1> <word2> ... <wordn>"`

- ### only display the most recent commit

  `git show`

  - #### display a specific commit's details
    
    `git show <commit-id>`
    
    `git show HEAD~3`
    
  - #### only display information of a specific commit
    
    `git show HEAD~6 --stat`
    
- ### display all commits sorted by author and title

  `git shortlog`
  
  - #### -s to show just the number of commits (rather than each commit's message) and -n to sort them numerically (rather than alphabetically by author name)

    `git shortlog -s -n`