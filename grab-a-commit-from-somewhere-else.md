## Given

A `<commit>` somewhere in the DAG. (Could be on the same branch, or on some
other branch, or not on a branch at all.)

## Expect

The `<commit>` to be applied to the tip of the current branch.

## Steps

    $ git cherry-pick <commit>

The `cherry-pick` command works fine with several commits too. They are applied
in order.

## Caveats

* `MIGHT_CONFLICT`
