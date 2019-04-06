# Working with remotes

Git is a version control tool.

GitHub is a service to host Git projects.

Remember that it's incredibly helpful to make all of your commits on descriptively named topic branches. Branches help isolate unrelated changes from each other.

- ### let you manage and interact with remote repositories(display the remote repo's shortname)

  `git remote`

- ### display a little more verbose and show remote url after name

  `git remote -v`

- ### rename a repo's shortname

  `git remote rename <old> <new>`

- ### add a connection to a new remote repository
  
  We can use this method to keep track on other developers's repo while we are working at the same repo.

  `git remote add <shortname> <url>`

- ### sending commits

  `git push <remote-shortname> <branch>`

  - #### force push

    `git push -f <remote-shortname> <branch>`

- ### pull changes from a remote
  
  - the commit(s) on the remote branch are copied to the local repository
  - the local tracking branch is moved to point to the most recent commit
  - the local tracking branch is merged into the local branch 

  `git pull <remote-shortname> <branch>`

- ### fetch changes from a remote

  - the commit(s) on the remote branch are copied to the local repository
  - the local tracking branch (e.g. origin/master) is moved to point to the most recent commit

  `git fetch <remote-shortname> <branch>`

- ### forking a repository

  Forking is an action that's done on a hosting service, like GitHub. Forking a repository creates an identical copy of the original repository and moves this copy to your account. You have total control over this forked repository. Modifying your forked repository does not alter the original repository in any way.

- ### CONTRIBUTING.md File
  
  The name of the `CONTRIBUTING.md` file is typically written in all caps so that it's easily seen. As you could probably tell by its name, this file lists out the information you should follow to contribute to the project. You should look for this file before you start doing development work of any kind.

- ### GitHub Issues

  Now, "issues" doesn't mean that there's actually a bug, it can just be any change that needs to be made to the project. GitHub's issue tractor is quite sophisticated. Each issue can:

  - have a label or multiple labels applied to it
  - can be assigned to an individual
  - can be assigned a milestone (for example the issue will be resolved by the next major release)

  Before you contribute anything to a file, check out the instructions in CONTRIBUTING.md. Then check out the project's issues and look to see if there's anything that's similar to what you want to contribute. If there is, then subscribe to that issue and read the existing conversation to see if you can help.

- ### Tips for working as contributor on GitHub

  Before you start doing any work, make sure to look for the project's CONTRIBUTING.md file.

  Next, it's a good idea to look at the GitHub issues for the project

  - look at the existing issues to see if one is similar to the change you want to contribute
  - if necessary create a new issue
  - communicate the changes you'd like to make to the project maintainer in the issue

  When you start developing, commit all of your work on a topic branch:

  - do not work on the master branch
  - make sure to give the topic branch clear, descriptive name

  As a general best practice for writing commits:

  - make frequent, smaller commits
  - use clear and descriptive commit messages
  - update the README file, if necessary

- ### Create a pull request

  A pull request is a request for the source repository to pull in your commits and merge them with their project. To create a pull request, a couple of things need to happen:

  - you must fork the source repository
  - clone your fork down to your machine
  - make some commits (ideally on a topic branch!)
  - push the commits back to your fork
  - create a new pull request and choose the branch that has your new commits

- ### Stay in sync with source project
  
  - #### Starring a repo

    Starring is helpful if you want to keep track of certain repositories. But it's not entirely helpful if you need to actively keep up with a repositories development because you have to manually go to the stars page to view the repositories and see if they've changed.

  - #### Watching a repo

    Watching a repository will alert you to all activity. This way GitHub will notify you whenever anything happens with the repository like people pushing changes to the repository, new issues being created, or comments being added to existing issues.

  When working with a project that you've forked. The original project's maintainer will continue adding changes to their project. You'll want to keep your fork of their project in sync with theirs so that you can include any changes they make.

  To get commits from a source repository into your forked repository on GitHub you need to:

  - get the cloneable URL of the source repository
  - create a new remote with the `git remote add` command
    - use the shortname upstream to point to the source repository
    - provide the URL of the source repository
  - fetch the new upstream remote
  - merge the upstream's branch into a local branch
  - push the newly updated local branch to your origin repo

- ### Manage an active PR
  
  As simple as at may seem, working on an active pull request is mostly about communication!

  If the project's maintainer is requesting changes to the pull request, then:

  - make any necessary commits on the same branch in your local repository that your pull request is based on
  - push the branch to the your fork of the source repository

  The commits will then show up on the pull request page.

- ### Squash commits
  
  - #### move commits to have a new base

    The -i in the command stands for "interactive". You can perform a rebase in a non-interactive mode. While you're learning how to rebase, though, I definitely recommend that you do interactive rebasing.

    `git rebase -i HEAD~3`

  - #### edit the root commit
    
    `git rebase -i --root`

  Inside the interactive list of commits, all commits start out as pick, but you can swap that out with one of the other commands (`reword`, `edit`, `squash`, `fixup`, `exec`, and `drop`).

  I recommend that you create a backup branch before rebasing, so that it's easy to return to your previous state. If you're happy with the rebase, then you can just delete the backup branch!

 