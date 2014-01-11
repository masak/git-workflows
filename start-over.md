## Given

Some work in the working copy that has not been added yet.

## Expect

To discard that work, going back wholly or partially to the way things were at
the last commit.

## Steps

Either on files:

    git checkout -- <file1> <file2> ...

Or all the changes:

    git checkout -- .
