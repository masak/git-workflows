Here a catalogue of more or less common Git workflows.

The idea is something like this: people have *intents*, things they want to do
with Git. This catalogue translates those intents into well-defined sequences
of steps. Really, that is what a course should focus on, too: "you want to do
X? well, just follow steps A, B, and C." The understanding of the underpinnings
of steps A, B, and C is nice but secondary.

Each file contains three parts:

* A **given** part, describing the situation.
* A **expect** part, explaining the result needed.
* A **steps** part, listing the steps that need to be taken.

All the three parts are given in a sufficiently informal English, rather than a
dry/formal DSL. However, the idea is that they still contain enough unambiguous
information for (a) a motivated human to follow them, or (b) a motivated robot
to turn them into a DSL if needed.

Optionally, there may also be a **caveats** section, for example if the
workflow involves rewriting shared history.
