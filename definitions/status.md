# Status

* The git status command displays the state of the working directory and the staging area.
* It lets you see which changes have been staged, which haven’t, and which files aren’t being tracked by Git. 
* Status output does not show you any information regarding the committed project history. For this, you need to use ``git log``.
* The git status command shows the state of the working directory and the staging area.
* For example, this is the GIT status of the repository as I edit this file.

```
On branch defmasterbranch
Your branch is up to date with 'origin/defmasterbranch'.

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   definitions/status.md

no changes added to commit (use "git add" and/or "git commit -a")
```

* In just a few lines, this command has told me the following:
    * I am on the ``defmasterbranch`` branch
    * I haven't staged any files to be commited
    * One file in the project has been modified and must be staged and commited for the changed to be tracked by GIT
* As you can see, this command also tells you exactly what you should do next
    * Use ``git add <file>`` to stage the file
    * use ``git restore <file>`` to DELETE untracked changes
    * After using ``git add``, you can use ``git commit -a`` to commit your changes

## Sources and further reading

* https://www.atlassian.com/git/tutorials/inspecting-a-repository