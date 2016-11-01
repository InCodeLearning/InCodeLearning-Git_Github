## Getting and Creating Projects


## Basic Snapshotting

`git-mv` - Move or rename a file, a directory, or a symlink

`git mv [-v] [-f] [-n] [-k] <source> <destination>` rename  
`git mv [-v] [-f] [-n] [-k] <source> ... <destination directory>` move into existing directory

```bash
git mv <source> <destination> # rename a directory
```

### Undo last commit

```bash
git commit -m "Something terribly misguided"
git reset HEAD~
# edit files as necessary
git add ...
git commit -c ORIG_HEAD
```
# Tagging

```bash
# display tag history with one line or <num> lines annotation
git tag -n<num>
git tag -a v1.0 -m "my version 1.0 tagging message"
git show v1.0
# tags have to be explicity pushed to remote
git push origin v1.0
git push origin --tags
```
