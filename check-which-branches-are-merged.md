## Given

A branch `<upstream>`.

## Expect

To find out which branches are proper ancestors of `<upstream>`, and are good
candidates for branch deletion.

## Steps

    $ git checkout <upstream>
    $ git branch --merged

Note that the query is *relative*, which is why you have to `checkout` the
right branch first.

## Variants

    $ git checkout <upstream>
    $ git branch --no-merged
