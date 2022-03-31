#  Git & Workflow


# Intro

**<span style="text-decoration:underline;">Deliveries:</span>**


* What is git
* Why do you need VCS (why can't I just write code?)

**<span style="text-decoration:underline;">Reading materials:</span>**


* https://stackoverflow.com/questions/1408450/why-should-i-use-version-control

**<span style="text-decoration:underline;">Timing:</span>**



* DIY: 1.5h
* Frontal

# Basic terminology

**<span style="text-decoration:underline;">Deliveries:</span>**

* Repository
    * Working directory
    * Staging area
    * Local repo
    * Remote repo
* Branch


**<span style="text-decoration:underline;">Reading materials:</span>**

* [Learn the Basics of Git in Under 10 Minutes](https://www.freecodecamp.org/news/learn-the-basics-of-git-in-under-10-minutes-da548267cc91/)
(until Step 0 not including).
* [Git-ing started with Git](https://www.youtube.com/watch?v=Ce5nz5n41z4)


**<span style="text-decoration:underline;">Timing:</span>**


* DIY: 2.0h
* Frontal

**<span style="text-decoration:underline;">Drill:</span>**
* Create a repository and push changes from your working directory to the remote, then download this repository to another location on your computer.
    * Explain which commands you've used for each stage.
* Explain the difference between `my_branch` and `origin/my_branch`
* Explain the difference between `fetch` and `pull`

# Commands

**<span style="text-decoration:underline;">Deliveries:</span>**

* Clone
* Init
* Status
* Add
* Commit
* Push
* Fetch
* Pull
* Branch
* Checkout
    * -f
    * -b
* Revert
* Reset
* Rebase
    * -i
* Merge
* Cherry-pick
* Stash
    * pop
    * clear
    * list
* Blame
* Bisect
* Merge conflict (not a command)

**<span style="text-decoration:underline;">Reading materials:</span>**

* https://rogerdudler.github.io/git-guide/
* https://dzone.com/articles/top-20-git-commands-with-examples
* man page
* google


**<span style="text-decoration:underline;">Timing:</span>**

* DIY: 5.0h
* Frontal


**<span style="text-decoration:underline;">Drill:</span>**
* Explain the difference between using rebase and merge for combining branches and pros cons (google it)
* Play with an interactive rebase, try out all of the different options (run rebase -i on something)
* Explain the difference between revert and reset, and between a soft reset and a hard reset
* [GitLab Git Workshop](https://forge.etsi.org/rep/help/university/training/user_training.md) (this will also teach you merge conflicts)

# Special files

**<span style="text-decoration:underline;">Deliveries:</span>**
* .gitignore
* README.md
* Changelog
* Know that it exists
    * .gitattributes
    * .gitmodules

**<span style="text-decoration:underline;">Reading materials:</span>**
* google

**<span style="text-decoration:underline;">Timing:</span>**

* DIY: 0.5h

# Branching

**<span style="text-decoration:underline;">Deliveries:</span>**

* Why do we need branching?
* Commit hash
* HEAD
    * Relative ref
        * ^
        * ~
* Tags
    * Why do we tag?

**<span style="text-decoration:underline;">Reading materials:</span>**
* https://git-scm.com/book/en/v2/Git-Branching-Branching-Workflows
* google

**<span style="text-decoration:underline;">Timing:</span>**

* DIY: 3.0h
* Frontal


**<span style="text-decoration:underline;">Drill:</span>**
* Open [Learn Git Branching](https://learngitbranching.js.org) and do all the levels up to "moving work around" at the "main" part and then do the "remote" part.

# Workflow

**<span style="text-decoration:underline;">Deliveries:</span>**

* Tag
    * Semantic versioning
        * Pre-release
        * Build metadata
        * Range
    * lightweight vs annotated
* Merge request / pull request
* Workflows
    * Feature branches
    * Release branches
    * Environment branches
* Release
* Issues
* Milestone

**<span style="text-decoration:underline;">Reading materials:</span>**
* https://semver.org
* https://stackoverflow.com/questions/11514075/what-is-the-difference-between-an-annotated-and-unannotated-tag
* [GitFlow](https://nvie.com/posts/a-successful-git-branching-model/)
* [GitLab Flow article](https://docs.gitlab.com/ee/topics/gitlab_flow.html)
* google

**<span style="text-decoration:underline;">Timing:</span>**

* DIY: 3.5h
* Frontal
