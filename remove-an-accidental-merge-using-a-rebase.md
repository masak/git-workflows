## Given

A branch `<upstream>` and a branch `<current>`. A merge commit at the tip of
`<current>`, merging in `<upstream>`.

## Expect

The `<current>` branch to be rebased on `<upstream>`, instead of merged. The
merge commit to go away.

## Steps

    $ git checkout <current>
    $ git rebase <upstream>

Yes, it is that simple.
