# Section 2 GitFlow and Git Commands

GitFlow
========

Gitflow Workflow defines a strict branching model designed around the project release. This provides a robust framework for managing larger projects.  

Gitflow is ideally suited for projects that have a scheduled release cycle. This workflow doesn’t add any new concepts or commands beyond what’s required for the Feature Branch Workflow. Instead, it assigns very specific roles to different branches and defines how and when they should interact. In addition to feature branches, it uses individual branches for preparing, maintaining, and recording releases.



Git Terminology
============

* Repository -  contains all of the project files (including documentation), and stores each file's revision history. Repositories can have multiple collaborators and can be either public or private.

* Clone - is a copy of a repository that lives on your computer instead of on a website's server somewhere, or the act of making that copy. With your clone you can edit the files in your preferred editor and use Git to keep track of your changes without having to be online.

* Fork - is a personal copy of another user's repository that lives on your account. Forks allow you to freely make changes to a project without affecting the original. 

* Branch - is a parallel version of a repository. It is contained within the repository, but does not affect the primary or master branch allowing you to work freely without disrupting the live version. When you've made the changes you want to make, you can merge your branch back into the master branch to publish your changes.

* Commit - is a record of what files you have changed since the last time you made a commit. Essentially, you make changes to your repo (for example, adding a file or modifying one) and then tell git to put those files into a commit.

* Merge - takes the changes from one branch (in the same repository or from a fork), and applies them into another. This often happens as a pull request (which can be thought of as a request to merge), or via the command line.

* Checkout - is the act of switching between different versions of a target entity.

* Push - refers to sending your committed changes to a remote repository, such as a repository hosted on GitHub. For instance, if you change something locally, you'd want to then push those changes so that others may access them.

* Pull -refers to when you are fetching in changes and merging them. For instance, if someone has edited the remote file you're both working on, you'll want to pull in those changes to your local copy so that it's up to date.

* Remote - this is the version of something that is hosted on a server, most likely GitHub. It can be connected to local clones so that changes can be synced.

* Status - these checks are external processes, which run for each commit you make in a repository.

* Master Branch -  is a default branch, as you start making commits, you're given a master branch that points to the last commit you made. Every time you commit, the master branch pointer moves forward automatically.



_A list of Git commands_
========================
### Getting & Creating Repositories

| Command | Description |
| ------- | ----------- |
| `git init` | Initialize a local Git repository |
| `git clone ssh://git@github.com/[username]/[repository-name].git` | Create a local copy of a remote repository |
