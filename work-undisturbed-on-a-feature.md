## Given

A branch `<master>`.

## Expect

Work on a feature without disturbing the ongoing work of colleagues, and
without their ongoing work disturbing you.

## Steps

    $ git checkout -b <feature> <master>
    $ [make any number of commits]

## After
    
    $ git checkout <master>
    $ git pull
    $ git checkout <feature>
    $ git rebase <master>       # see also tidy-up-a-branch
    
    $ git checkout <master>
    $ git merge <feature>
    $ git branch -d <feature>

## Caveats

* `MIGHT_CONFLICT (the `rebase <master>` step)`
