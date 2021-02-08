# Remote Add / Remove / Show

* GIT uses a centralized repository to keep multiple developers in sync.
* The ``git remote`` command makes it possible to add, remove and manage remote repositories attached to your local repository.

## Add

* Use this command to add a remote repository that your local repo can sync to

```
git remote add <shortname> <url>
```

* ``<shortname>`` is the name of the remote, if this argument is ommited, it will default to origin


## Remove

* Use this command to remove a remote repository
* This command does not delete the remote repo, instead, it removed the link between the local and remote repo.
This means that you will no longer be able to push or pull changes from the remote repo

```
git remote remove <shortname>
```

* Ommiting the ``<shortname>`` will default to ``origin``
* Once you delete the reference to a remote this way, all remote-tracking branches and configuration settings associated with that remote are also deleted.

## show

* The ``git remote show`` command will simply display a list of remotes linked to your repository
* For example, running the command on this repository displays:
```
origin
```

## Sources and Further Reading
* https://git-scm.com/book/en/v2/Git-Basics-Working-with-Remotes