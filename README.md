# Me Learning Git
This is just a test repo to try different Git and Github related things out.

## Reset github repo to an earlier state via local repo
Sometimes I want to actually rewind a few steps in the repo history, usually for tidiness. **Note that this is permanent!**

1. Do a hard reset to a specific commit id `git reset --hard 1234abc`
1. Local will now say that there are commits to pull from origin (github) - do not pull these
1. Force push from local to github `git push -f origin master`
1. Local and origin (github) should now be identical

## Stash current edits and move them to a new branch
Often I realise my current work would have been better in a new branch:
1. Stash current edits `git stash push`
1. Create a new branch and unstash edits `git stash branch nameofnewbranch`

## Stash current edits, switch to an existing branch, and unstash
Often I realise my current work would have been better in a different branch that already exists:
1. Stash current edits `git stash push`
1. Switch to a different branch
1. Unstash edits `git stash pop`

## Stash current edits including untracked (new) files
`git stash push -u`
