## Given

A `<file>` sitting on a branch `<other-branch>` which you're currently not on.

## Expect

The contents of `<file>` on `<other-branch>` to be put into the working copy.

## Steps

    $ git checkout <other-branch> -- <file>
