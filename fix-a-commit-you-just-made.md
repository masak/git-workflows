## Given

    $ git commit

## Expect

The commit (with some mistakes or omissions) to be *replaced* with a slightly
better one.

## Steps

    $ $EDITOR file1 file2 ...
    $ git add file1 file2 ...
    $ git commit --amend

## Caveats

REWRITE_HISTORY
