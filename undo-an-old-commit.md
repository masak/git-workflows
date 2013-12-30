## Given

An old `<bad-commit>` appearing upstream of your current branch tip.

## Expect

The changes of the old commit to be undone in a new commit. (The old commit
will remain in history, but a new "anti-commit" will be created.)

## Steps

    $ git revert <bad-commit>

You can revert as many commits as you like. It is strongly advised that you
revert them in the *reverse* order they were applied the first time, as this
best preserves context.

## Caveats

* `MIGHT_CONFLICT`
