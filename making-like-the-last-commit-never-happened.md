## Given

A `<commit>` just made on the current branch.

## Expect

That commit not to exist on the branch any more.

## Steps

    $ git reset --hard HEAD^

## Caveats

REWRITE_HISTORY
HARD_MEANS_HARD
