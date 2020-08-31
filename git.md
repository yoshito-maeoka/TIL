# stash partly
```
git stash -p
```

# use specific account on a specified project
```
$ cd a_specified_prj
$ git config user.name hogehoge
$ git config user.email hogehoge@example.com

```
# search deleted files from history
git log --diff-filter=D --summary


# merge problem

when this message appeared:
```
fatal: refusing to merge unrelated histories
```
use with this options
```
git merge <branch-name> --allow-unrelated-histories
```


# set the existing branch upstream branch.

```
git branch -u <remote>/<branch>
```