# Learn Git

_Practice_

If the instructions below are too terse, you should instead follow along with Software Carpentry's excellent [Git novice tutorial](https://swcarpentry.github.io/git-novice/). If they're too easy, skip to the last exercises. If they're still too easy, challenge yourself to learn a new Git workflow or feature.

1. Try out basic Git workflows on the command line:
    - First initialize a Git repository by doing `git init` or `uv init` inside a dedicated folder.
    - Write some dummy code in some file.
    - Tell Git to start tracking that file by `git add <filename>`.
    - Commit it with a message explaining what changes have been done since last by `git commit -m "Add feature this and that"`
    - Make some more updates to the same file or another file.
    - Check status and changes with `git status` and `git diff`.
    - Add, commit. Check log with `git log`.
    - Make another change to one file. Realise you messed up and want to revert to the last committed version: `git restore <filename>`.
    - Create and checkout a new branch, `git checkout -b <branchname>`. Create a new file, stage (add) and commit it. Go back to the main, branch `git checkout main`, and see the new file is no longer there. Merge the new branch into main, `git merge <branchname>`. Delete the new branch, `git branch -d <branchname>`.


2. Now try doing the same actions in the version control interface of your editor of choice. If using Jupyter Lab, you need the jupyterlab-git extension.

3. Practice keeping a local repository in sync with a Github-hosted repository. 
    - Start by creating a new repository on Github (this can be private). It's a good idea to include the suggested Python .gitignore file.
    - Copy the repository address from the green "Code" button and do, in your terminal `git clone <pasted-address>`
    - Check that your local repository is tracking the Github remote by `git remote -v`.
    - Write some dummy code and commit it. Then push to Github by `git push`.
    - On Github web, change one of the files and commit. Back in your local repo (in terminal), pull this change.
    - Create (checkout) a branch, do some changes there, push to remote, and merge back into the main branch.

4. Try to create conflicting edits in different branches or locally and remote. See what happens when you try to checkout or pull the conflicting branch/remote. How do you solve the conflict?

5. If you're done or all of this is too easy, try looking into some of the more esoteric functions of git, for example by looking [here](https://ndpsoftware.com/git-cheatsheet.html) (should be safe although there's a certificate problem).

6. Alternatively, learn about how to use [pull requests](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/about-pull-requests) or [issue tracking](https://docs.github.com/en/issues/tracking-your-work-with-issues/about-issues) (which can also be used for keeping track of todos and bugs on personal projects). 