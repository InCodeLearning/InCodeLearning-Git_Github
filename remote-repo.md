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
