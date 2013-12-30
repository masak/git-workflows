## Given

A branch `<branch>` and an arbitrarily placed `<commit>`, maybe earlier on the
chain of `<branch>` commits, or maybe somewhere else entirely in the DAG.

## Expect

To place the tip of `<branch>` on `<commit>`.

## Steps

    $ git branch -f <branch> <commit>

## Caveats

* `REWRITE_HISTORY`
