Strongly typed semantic versioning
==================================

[Semantic versioning][1] is a popular scheme for versioning projects in modern
languages, especially where quick iteration is a goal. `elvysh` uses a modified
variant I call strongly typed semantic versioning, where due to compiler
guarantees we can define four useful version components instead of three.

Strongly typed semantic versioning consists of version numbers like
`SUPER-MAJOR.MAJOR.MINOR.PATCH`. If a change is a backwards compatible bug fix,
doc improvement, etc., the `PATCH` number should be incremented. If a change
adds functionality but in a completely backwards-compatible way, the `MINOR`
number should be incremented. If a change is not completely backwards
compatible, *but* all such incompatibilities will be caught at compile time
(e.g. changing the type signature of a function), then the `MAJOR` number should
be incremented. Finally, if a change is not completely backwards-incompatible
in such a way that a previously working program would still compile but would
behave wrong, then the `SUPER-MAJOR` number should be incremented. Whenever a
version component is incremented, all components to the right of it should be
reset to `0`.

Finally, for `elvysh` projects, version numbers start at `1.0.0.0` to encourage
good iterative incremental work right from the start.

[1]: http://semver.org/
