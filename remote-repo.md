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
