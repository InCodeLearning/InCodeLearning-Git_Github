Category reference [git official docs](https://git-scm.com/docs/). Or click "Topics" on any git command official doc.

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

### Modify last commit

```bash
# update last commit's time to right now
GIT_COMMITTER_DATE="`date`" git commit --amend --date "`date`"
# will bring up window to modify last commit's commit message
git commit --amend
```

## Tagging

```bash
# display tag history with one line or <num> lines annotation
git tag -n<num>
# annotated tags
git tag -a v1.0 -m "my version 1.0 tagging message"
git show v1.0
# lightweight tags, aliase to a commit, no extra message
git tag v1.1-lw
# tags have to be explicity pushed to remote
git push origin v1.0
git push origin --tags
# display detailed tag information
git for-each-ref --sort -v:refname --format '%(objectname) %(objecttype) %(refname) %(contents) %(*objectname) %(*objecttype) %(*refname) %(*contents)' refs/tags | grep commit
# tagging later
git log --pretty=oneline
git tag -a v1.2 9fceb02 # first 7 digits of hash (sha-1)
```
