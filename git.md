## Git

<!---
    // TODO: table of contents

    https://try.github.io/levels/1/challenges/18
    https://github.com/robbyrussell/oh-my-zsh/wiki/Plugin:git
-->

### Init

Initializes a repository in an existing directory. This will create `.git` hidden folder, a location where Git operates.

```
git init
```


### Status

Shows the working tree status.

```
git status
```

### Add

This command updates the index using the current content found in the working tree, to prepare the content `staged` for the next commit.

```
git add some-file.txt
```

Wildcards are supported, e.g. `git add '*.txt'` or you can add all files by `git add .`

### Commit

Check how to properly write a git [commit message](http://chris.beams.io/posts/git-commit/).

Records changes to the repository. By using `-m` flag, a custom message will be added with commit.

```
git commit -m "Some message"
```

By using `-a` flag, command will also do `git add .`

```
git commit -a -m "Some message"
```

### Log

Shows commit logs.

```
git log
```

### Remote add

Manages set of tracked repositories.

```
git remote add origin some-url
```

### Push

Updates remote refs along with associated objects. The flag `-u` tells Git to remember the parameters, so that next time we can simply run git push and Git will know what to do.

```
git push -u origin master
```

### Pull

Fetches from and integrate with another repository or a local branch.

```
git pull origin master
```

### Diff

Show changes between commits, commit and working tree, etc.

```
git diff
```

Shows difference of most recent commit, which is referred using the HEAD pointer.

```
git diff HEAD
```

Shows staged difference.

```
git diff --staged
```


### Reset

Unstages files.

```
git reset some-file.txt
```

Flag `soft` will move HEAD 1 commit back and put changes as they were not commited yet, so you can commit them again.

```
git reset --soft HEAD~1
```

Flag `hard` will move HEAD 1 commit back and delete changes.

```
git reset --hard HEAD~1
```

### Revert

It will revert commit by adding a commit (so you can see the history of what has been reverted).

```
git revert commitId
```

### Checkout

Changes file back to how it was at the last commit.

```
git checkout -- some-file.txt
```

### Submodules

Go to root folder.

```
git submodule add some-repo-url some-folder
```

<!---

// TODO

### Merge

git merge --abort

Reset, Checkout, and Revert
https://www.atlassian.com/git/tutorials/resetting-checking-out-and-reverting/commit-level-operations

Check and document those commands.

git branch new_branch_name
git checkout new_branch_name
git merge name_of_branch (checkout to master to merge development branch)
git branch -m old_branch_name new_brach_name (renaming branch)
git branch --merged (showing merged branches that had been merged at any time)
git branch --no-merge (just the opposite as above command)
git branch -d branch_name (deleting branch)

https://chrisjean.com/git-submodules-adding-using-removing-and-updating

-->
