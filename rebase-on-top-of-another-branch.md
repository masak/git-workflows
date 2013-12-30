## Given

Three branches:

* `<master>`.
* `<A>`, branched from `<master>`, containing some commits.
* `<B>`, branched from `<A>`, containing some commits.

## Expect

`<B>` to be branched from `<master>`, not `<A>`.

## Steps

    $ git checkout <B>
    $ git rebase --onto <master> <A>

## Caveats

REWRITE_HISTORY
MIGHT_CONFLICT
