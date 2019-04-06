# Configuration

- ### sets up Git with your name
  `git config --global user.name "<Your-Full-Name>"`

- ### sets up Git with your email
  `git config --global user.email "<your-email-address>"`

- ### makes sure that Git output is colored
  `git config --global color.ui auto`

- ### displays the original state in a conflict
  `git config --global merge.conflictstyle diff3`

- ### view configuration
  `git config --list`

- ### get Git working with code editor

  #### MAC/Linux

  - #### Atom Editor Setup
    `git config --global core.editor "atom --wait"`

  - #### Sublime Text Setup
    `git config --global core.editor "'/Applications/Sublime Text 3.app/Contents/SharedSupport/bin/subl' -n -w"`

  #### Windows

  - #### Atom Editor Setup
    `git config --global core.editor "atom --wait"`

  - #### Sublime Text Setup
    `git config --global core.editor "'C:/Program Files/Sublime Text 2/sublime_text.exe' -n -w"`