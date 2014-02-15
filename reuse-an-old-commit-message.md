# Given

An old `<commit>`, not necessarily the last one or even on the current branch.

# Expect

To re-use commit message and author name/email/timestamp information from the
old `<commit>`, but without the commit itself being an actual `cherry-pick`.

# Steps

    $ git commit -C<commit>
