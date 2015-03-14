Project standards
==================

Libraries in the `elvysh` project should follow the following standards:

* Each individual library should have overview documentation explaining what
  it is for.
* All top-level function and type definitions should be commented, including
  describing parameters, return values, and semantics.
* Files simply meant to be loaded/included (.sats, .hats, .dats that only
  implement partial template specializations) should live in `include/elvysh/`
* Files meant to be compiled directly and linked in with the result should live
  in `src/`
* Global state should be avoided if at all possible. If not, access should be
  mediated via views similar to [elvysh-errno][1].
* To the extent possible, all pre- and post-conditions of functions should be
  made clear in the types, with proofs and views where applicable.
* Unless it is inherent in the library's purpose, no use of the ATS runtime's
  garbage collection or compiler-boxed types.
* Every commit on `master` should be a valid release. If some change requires
  multiple logical commits, they should be done in a branch and merged in (with
  `--no-ff`).
* Because git revisions are not useful to users of the libraries, each release
  (that is, each commit directly on `master`) should be tagged with a version
  according to [strongly-typed semantic versioning][2]
* Where applicable, `ATS_EXTERN_PREFIX` and `ATS_PACKNAME` should be defined to
  `"elvysh_<libname>_"`, where `<libname>` is replaced with the name of the
  library.
* The coding standard is not explicitly delineated yet, but code should be
  similar in style to other libraries in the project.
* Once this becomes relevant, dependencies on other libraries in the project or
  external tools and libraries should be handled uniformly.

[1]: https://github.com/shlevy/elvysh-errno
[2]: strongly-typed-semver.md
