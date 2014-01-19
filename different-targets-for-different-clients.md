## Given

Several different "flavors" of the same product; some features present in some
of the flavors, others not. This is richer than just several different versions
that can be sorted along the same timeline. Each flavor has its own timeline
along which it evolves. The situation is further complicated by the fact that
sometimes changes happen on just a single one of the flavors, but sometimes it
happens on several or all of them.

## Expect

To be able to quickly modify, build, or release any of the flavors.

## Steps

There are two major ways to handle this:

1. **One branch, many build targets.** Keep things together as one single code
base. Optionally have script that "derive" the different versions from the
single code base.

2. **Several branches, one per flavor.** Dedicate one branch per flavor.

Favor the first approach as much as possible. Yes, there is some additional
machinery that needs to be built and maintained for those scripts and build
targets, but keeping one code base together in one branch is a lot more
pleasant than keeping N code bases together in N branches. The risk of the
latter approach is the same kind of risk as with making updates on a
denormalized database.
