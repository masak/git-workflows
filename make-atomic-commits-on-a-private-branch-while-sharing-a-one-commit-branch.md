## Given

Two branches `<master>` and `<private-many>`, the latter branching off the
former.

## Expect

To create and share a `<public-one>` branch, with the same changes as in
`<private-many>`, but contained in a single commit.

(This is a common workflow with for example Gerrit.)

## Steps

    $ git checkout -b <public-one> <private-many>
    $ git rebase -i             # squash all commits except the first
    $ git push -u origin public-one

## After

If you are likely to come back to the `<private-many>` branch to do some work
that you will later share again in the same way, consider sharing it on
*another* public branch label to avoid confusion among your downstream
consumers. Consider establishing a naming scheme.

    $ git push -u origin public-one-v1
    $ git push -u origin public-one-v2
    $ git push -u origin public-one-v3
    $ git push -u origin public-one-v4

## Variants

See also `git rebase --squash` and `git merge --squash`.

In fact, you can acheive the moral equivalent with the following `reset`-based
workflow:

    $ git checkout -b <public-one> <private-many>
    $ git reset --soft <master>
    $ git commit
    $ git push -u origin public-one
