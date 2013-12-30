## Given

Two branches, `<master>` and `<feature>`.

## Expect

To compare them, learning what commits have been made on one branch but not
another.

## Steps

All steps are optional, and order doesn't matter.

    $ git diff <master>..<feature>  # what happened on <feature>?
    $ git diff <feature>..<master>  # what happened on <master>?

If you're already on the `<feature>` branch, you can abbreviate it to this:

    $ git diff <master>..           # what happened on HEAD=<feature>?
    $ git diff ..<master>           # what happened on <master>?

If you're already on the `<master>` branch, you can abbreviate it to this:

    $ git diff ..<feature>          # what happened on <feature>?
    $ git diff <feature>..          # what happened on HEAD=<master>?

## After

After doing one or more of these comparisons, you might want to continue by
merging:

    $ git checkout <master>
    $ git merge <feature>

Or rebasing:

    $ git checkout <feature>
    $ git rebase <master>
