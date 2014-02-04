## Given

A branch `<branch>`, and a commit `<commit>` which is on `<branch>` but isn't
pointed to by `HEAD`.

## Expect

To do the equivalent of `git commit --amend`, but on `<commit>`, not on `HEAD`.

## Steps

    $ git checkout <branch>
    $ git rebase -i <commit>^   # and change 'pick' on the first line to 'reword' or 'edit'
    $ # make the appropriate changes to the commit
