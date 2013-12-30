## Given

A `<file>` that has been touched by many commits, and a certain change or
feature or bugfix in that file.

## Expect

To find the commit where the change or feature or bugfix was first added.

## Steps

    $ git blame <file>          # extract a <commit> from the blame output

Now the `<commit>` you find will either be The One, at which point you can
inspect it to your heart's content:

    $ git show <commit>

Or it will just be an insignificant change to the original thing you're
interested in, at which point you start from the commit *before*, and repeat as
many times as necessary:

    $ git checkout <commit>^
    $ git blame <file>

(The `<file>` may have changed its name on the way.)

## After

You will want to get back to where you were when you started:

    $ git checkout <some-branch>
