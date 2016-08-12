## Actual workflow:

1. Make sure you are on your own branch with `git branch`. When you first join the team, you will be assigned a branch named with your first name or preferred name. Please keep using this branch. `git checkout -b origin/<branch_name>` to start using your branch.
2. **Merge `dev` into your branch `git merge dev`.**
  1. Warning: `git mergetool` might be needed for resolving conflicts if you did no follow this flow exactly. Alternatively you could resolve the conflicts manually one file by one file.
3. Do your edits and commits and `git push`.
4. Create pull request (PR) merging from your own branch into `dev` branch.
Do more commits if you would like to. The later commits would be automatically included in the PR. Now all other team members should read your PR and comment their questions or suggestions for you.
5. On weekly video hangout conference we will discuss each member's PR.
6. After weekly meeting, Jesse will merge all the branches into `dev` within two days, i.e., if meeting was on Sunday, merge will be done before Tuesday.
7. **ONLY Jesse can merge from `dev` to `master`.**

If you are interested in learning git and github, you are welcome to join Jesse in maintaining this repo and join the administrator team to do the tasks for merging all branches into `dev` branch weekly. The homeworks below should help you learn more about git.

### Github Work-Flow Homework

1. Create a repo in your github account and then create a `dev` branch off from `master` branch. Do some commits on `dev` branch and push it to github.
2. Create a branch off from `dev` branch **(note important: not from `master` branch)** with your own name as the branch name.
3. Do edits and some commits in your own branch and push to github.
4. Create a pull request (PR), merging from your own branch into `dev`. Stop here and we will have a video/voice google hangout session to test that you fully understood the workflow. Send Jesse the link of your testing repo.
5. Merge the PR on the command line.

### Git Merge Resolving Conflict Homework

Mimic what happened in this tree of commits and merge [here](https://github.com/InCodeLearning/git-test/commits/dev).

Share with us whether you resolved the conflict manually one file by one file or used a `mergetool`. Which `mergetool` did you use? We would love to see some screen shots of your `mergetool`. Did you like the `mergetool` you used?

## Resources

* just google git cheatsheet
* [progit book](https://git-scm.com/book/en/v2)
