## Given

A branch `<feature>` with at least `<N>` commits.

## Expect

To see a list of just the last `<N>` commits on the `<feature>` branch, even if
there are more.

## Steps

    $ git log <feature>~<N>..<feature>

If you're already on the `<feature>` branch, you can abbreviate to this:

    $ git log HEAD~<N>..

## Variants

Or let's say you're interested in seeing the past three days of work. Then you
can specify a "human date" component:

    $ git log --since='3 days ago' <feature>

Or, if you're already on the right branch:

    $ git log --since='3 days ago'
