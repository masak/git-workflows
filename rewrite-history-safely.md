## Given

An already-shared `<branch>`, and a `<command>` you want to do that rewrites
the history of that branch.

## Expect

To rewrite the commits of `<branch>`, but without running into all the problems
associated with rewriting shared history.

## Steps

It's perfectly fine to rewrite history, as long as you do it with *a new branch
label*.

    $ git checkout -b <rewrite> <branch>
    $ <command>
    $ git push -u origin <rewrite>
