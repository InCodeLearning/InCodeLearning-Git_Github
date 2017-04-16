## Branching

`git branch [options] <branchname>`

```bash
git branch # show all branches with current marked with *
git branch -vv # show all local and tracked remote branches
git checkout dev
git branch jesse
# creates branch named "jesse" off from "dev" branch
git checkout -b jesse
# creates and switch to branch "jesse"
```

## Merging

`git merge [options] [<commit>...]`  
`git merge --abort` may not be able to fully recover

```bash
git merge --no-ff
# no fast forwarding creates merge commit for FF
git merge jesse
# merge commits on jesse into current branch
```

## Rebasing

```
git pull --rebase # may resolve upstream squashing commits, many use as default
git config --global pull.rebase true # to set as default
```

References:

[when to use `git pull --rebase`](http://stackoverflow.com/questions/2472254/when-should-i-use-git-pull-rebase)
