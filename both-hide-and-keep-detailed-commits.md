## Given

Two branches:

* `<master>`
* `<A>`, branched from `<master>`, containing some commits.

## Expect

The commits from `<A>` to be merged into `<master>` as a single commit, without
being squahed.

## Steps

    $ git checkout <master>
    $ git merge --no-ff <A>

Idea comes from #perl6:

    <nwc10> tadzik/moritz: the trick we were using in perl 5 was to force a non-ff merge
    <nwc10> so you end up with a merge commit, the left parent of which is to the start of a run of related commits
    <nwc10> and the right parent of which is the run of commits
    <nwc10> so the left parent is the "squashed" commit (and the default that most things see)
    <nwc10> but the branch to the right preserves the detail
    <tadzik> sounds nice

