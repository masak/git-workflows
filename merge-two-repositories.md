# Given

A remote repository `<B>` tied to the current repository `<A>`.

# Expect

`<A>` to contain the histories of both `<A>` and `<B>`, joined together with a
merge commit.

# Steps

    $ git fetch <B>         # you will get a warning about no commits in common
    $ git merge FETCH_HEAD
