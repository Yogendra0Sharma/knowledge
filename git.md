## Git

<!---
    https://try.github.io/levels/1/challenges/10
-->

### Init

`git init`

Initializes a repository in an existing directory. This will create `.git` hidden folder, a location where Git operates.

### Status

`git status`

Shows the working tree status.

### Add

`git add some-file.txt`

This command updates the index using the current content found in the working tree, to prepare the content `staged` for the next commit.

Wildcards are supported, e.g. `git add '*.txt'` or you can add all files by `git add .`


### Commit

`git commit`

Records changes to the repository.

`git commit -m 'Some message'`

By using `-m` flag, a custom message will be added with commit.

### Log

`git log`

Shows commit logs.
