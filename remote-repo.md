This markdown file summarizes all git commands working with remote repositories such as github or bitbucket.

`git fetch [<options>] [<repository> [<refspec>]]`

```bash
git fetch origin # fetch branches and/or tags from "origin" remote
git fetch -a # fetches from all remotes
```

`git remote [-v | --verbose]`  
`git remote add [-f] [--[no-]tags] <name> <url>`

```bash
git remote # show all remote repositories
git remote -v # show all remote repositories with urls

# add remote repo and name it origin
git remote add origin https://github.com/user/repo.git
# runs git fetch origin immediately after
git remote add -f origin https://github.com/user/repo.git
# change remote repo url, useful when you renamed github repo
git remote set-url origin https://github.com/InCodeLearning/InCodeLearning-Git_Github.git
```

### Merge a Pull Request on Github

Step 1: From your project repository, bring in the changes and test.

```bash
git fetch origin
# not necessary if you just pushed local 
git checkout -b lname origin/rname 
git merge dev
```

Step 2: Merge the changes and update on GitHub.

```bash
git checkout dev
git merge --no-ff jesse # no fast fowarding, create a merge commit
git push origin dev
```

### Pull All Remote Branches

```bash
# the first line creates local branch with same name tracking remote branch
git branch -r | grep -v '\->' | while read remote; do git branch --track "${remote#origin/}" "$remote"; done
git fetch --all
git pull --all
```

### Delete a Remote Branch

```bash
git push origin --delete <branchName>
```

### Clear stale remote branches

You deleted some remote branches however they still show up in `git branch -r`.

```bash
git remote prune origin
```

### Undo a git push

Generally you should avoid at all cost pushing wrong things. But if you have to,

```bash
git push -f origin last_known_good_commit:branch_name
git push -f origin 133fe1b8b7745a9f91fc90e556100fa87c87d00c:master
``` 
