# Given

Two branches, `<upstream>` and `<downstream>`.

# Expect

The tree of `<downstream>` to be like that of `<upstream>`, but without any
history rewriting.

# Steps

The below method is really a five-command way to compensate for the lack of a
merge strategy `--theirs` in Git.

    $ git checkout -b tmp <upstream>
    $ git merge -s ours <downstream>        # ignore all changes in <downstream>
    $ git checkout <downstream>
    $ git merge tmp                         # fast-forward to tmp HEAD
    $ git branch -D tmp                     # deleting tmp

[This SO
answer](http://stackoverflow.com/questions/4911794/git-command-for-making-one-branch-like-another)
contains five alternative ways to do the same thing.
