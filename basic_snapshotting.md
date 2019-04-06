# Basic snapshotting

- ### move files from the Working Directory to the Staging Index
  
  `git add <file-name> <file-name>`

  - #### stage the remaining files

    `git add .`

- ### unstage

  `git rm --cached <file-name>`

- ### takes files from the Staging Index and saves them in the repository and open the code editor that is specified in your configuration

  `git commit`

  - #### commit the remaining files

    `git commit .`

  - #### commit bypass editor(it won't open the code editor)
    
    `git commit -m <msg>`

- ### see changes that have been made but haven't been committed, yet

  `git diff`

- ### having Git ignore files
  
  create a specially named file .gitignore in the same directory that the hidden .git directory is located to tell Git about the files that Git should not track
  
  `touch .gitignore`

  - Adding files that want to be ignored in the .gitignore file
  - Globbing - lets us use special characters to match patterns/characters
  - blank lines can be used for spacing
  - '\#' - marks line as a comment
  - '\*' - matches 0 or more characters
  - '?' - matches 1 character
  - '\[abc\]' - matches a,b,_or_c
  - '\*\*' - matches nested directories - a/**/z matches(a/z, a/b/z, a/b/c/z)
