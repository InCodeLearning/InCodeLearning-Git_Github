## Github Work-Flow Homework

1. Create a repo in your github account and then create a `dev` branch off from `master` branch. Do some commits on `dev` branch and push it to github.
2. Create a branch off from `dev` branch **(note important: not from `master` branch)** with your own name as the branch name.
3. Do edits and some commits in your own branch and push to github.
4. Create a pull request (PR), merging from your own branch into `dev`. Stop here and we will have a video/voice google hangout session to test that you fully understood the workflow. Send Jesse the link of your testing repo.
5. Merge the PR on the command line.

### Actual workflow:

1. Make sure you are on your own branch with `git branch`, create your own branch from `dev` if your branch not yet exists.
2. Merge `dev` into your branch `git merge dev`.
3. Do your edits and commits.
4. Create pull request (PR) merging from your own branch into `dev` branch.
Do more commits if you would like to. The later commits would be automatically included in the PR. Now all other team members should read your PR and comment their questions or suggestions for you.
5. On weekly video hangout conference we will discuss each member's PR.
6. Every week we will take turns do merging everyone’s branch into `dev`.
  1. Warning: `git mergetool` is needed for resolving conflicts easily. Alternatively you could resolve the conflicts manually one file by one file.
7. **ONLY Jesse can merge from `dev` to `master`.**

## Git Merge Resolving Conflict Homework

Mimic what happened in this tree of commits and merge [here](https://github.com/InCodeLearning/git-test/commits/dev).

Share with us whether you resolved the conflict manually one file by one file or used a `mergetool`. Which `mergetool` did you use? We would love to see some screen shots of your `mergetool`. Did you like the `mergetool` you used?
