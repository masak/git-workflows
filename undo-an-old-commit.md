## Given

An old `<bad-commit>` appearing upstream of your current branch tip.

## Expect

The changes of the old commit to be undone in a new commit. (The old commit
will remain in history, but a new "anti-commit" will be created.)

## Steps

    $ git revert <bad-commit>

## Caveats

MIGHT_CONFLICT
