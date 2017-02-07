## Git Setup and Configuration

```bash
# list all configurations
git config -l # --list
```

```bash
# only push current branch to the one it pulls from
git config --global push.default=simple
git config --global user.name "Jesse Zhuang"
git config --global user.email "JesseDoe@gmail.com"
```
password storage
SSH allows key without passphrase, no username/password needed.
```bash
# save for 15 min
git config --global credential.helper 'cache --timeout=900'
# use wincred on Windows
git config --global credential.helper wincred
```
