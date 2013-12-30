## Given

A local branch `<master>`, and a remote `<frank>` with a branch
`<frank/master>`.

Some commits on each of the branches `<master>` and `<frank/master>`, meaning
that they diverged from each other.

## Expect

The work done on `<frank/master>` to be applied onto `<master>` without having
to merge the two branches.

## Steps

    $ git checkout -b franks-work <frank/master>
    $ git rebase master
    $ git checkout master
    $ git merge franks-work     # will be a fast-forward

## After

    $ git push                  # probably the next step

## Caveats

* `MIGHT_CONFLICT`
