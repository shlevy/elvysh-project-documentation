Project goals
=============

`elvysh` libraries are built with the following goals/principles in mind:

* Ensuring correctness through proofs. To whatever extent possible, all
  properties and preconditions of functions and values are encoded in their
  types.
* Don't pay for what you don't need. Minimal runtime cost and doing as much work
  at compile time as possible.
* Code reuse wherever possible. Don't reinvent the wheel, break work up into
  logical modular parts.
* Find points for improvement in ATS. It's expected that extensive use of ATS
  for real projects will uncover places where the core language can be improved.
* Provide a common framework for working on ATS projects. It should be possible
  to look at an `elvysh` library and know exactly how to build it, integrate it
  into your projects, etc.
* Focus on practicality. There are a lot of fun experiments you can do with ATS,
  I've done more than my fair share, but `elvysh` libraries are meant to be
  used.
* Incremental progress. Any even marginally useful creation/change should be
  made available, as long as the overall path is toward the goals of the
  library.
* Other-developer friendly. Clean code, complete documentation, and good
  interfaces.
