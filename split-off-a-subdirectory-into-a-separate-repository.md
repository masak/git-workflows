# Given

A subdirectory `<separate>` in the current repository `<original>`, tracked by
Git and with an interesting commit history.

# Expect

To split the history of the `<separate>` directory into a repository of its
own, containin only the commits that pertain to that directory. (And with the
directory itself gone, with only its contents remaining.)

# Steps

    $ cd ..
    $ git clone <original> <separate>       # name the clone after the dir
    $ cd <separate>
    $ git filter-branch --prune-empty --subdirectory-filter <separate> -- --all
    $ git clone <separate> <separate>-new   # this clone leaves old commits behind
