## Given

Two branches, `<master>` and `<feature>`, the latter branching off the former.

## Expect

Some bad commits to be skipped or improved before merging the branch
`<feature>` into `<master>`.

## Steps

    $ git checkout <feature>
    $ git rebase -i <master>

## After

You can do that latter step as many times as you like. If you find yourself in
the middle of a rebase you would like to abort, just do this:

    $ git rebase --abort

If you want to undo a rebase you just did, you can use the special symbol
`ORIG_HEAD` (which the `rebase` command sets):

    $ git reset --hard ORIG_HEAD

## Caveat

REWRITE_HISTORY
HARD_MEANS_HARD
