## Given

Two branches, `<source>` and `<destination>`, with divergent histories.

## Expect

To put the contents of `<source>` into the `<destination>` branch, without
rewriting history.

## Steps

    $ git clean -dfx
    $ git checkout <destination>
    $ git reset --hard <source>
    $ git reset --soft ORIG_HEAD
    $ git add -Af .
    $ git commit -m "Rewrite <destination> with <source>"
    $ git merge -s ours <source>
