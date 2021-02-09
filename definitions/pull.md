# Pull

* The ``git pull`` command is used to fetch and download content from a remote repository and immediately update the local repository to match that content.
* The ``git pull`` command first runs ``git fetch`` which downloads content from the specified remote repository. Then a ``git merge`` is executed to merge the remote content refs and heads into a new local merge commit.

```
git pull <remote>
```
* If you omit ``<remote>``, the command will pull from ``<origin>``

## Sources and further reading

* https://git-scm.com/docs/git-pull