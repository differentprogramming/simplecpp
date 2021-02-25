# differentprogramming:
Forked to be part of a C to Advanced Common Runtime, a name I just came up with for what will be something like the JVM or CLR but with every feature and the kitchen sink thrown in. For example features missing from JVM and CLR are image based persistence, tail call optimization, go routines, multiple dispatch, delimited continuations, non-determinism, logical variables, reified search, logical programming, pattern-based or where-clause tested dispatch, multiple return values, LLVM codes as a generic inline assembler, support for live schema alterations (ie cleanup routines for changing a running program), and a low latency garbage collector like Go. Wish me luck!

Although the project is open source I don't want to be infected with LGPL, so this library will be dynamically linked.

Planned changes to the original:
1) output to an internal stream to the linking program instead of to the disk.
2) being given virtual input directories by the linking program instead of reading from the disk.
3) if possible, create or include a side channel of original token position data - or at very least the preprossessed line being expanded.

# Simple C/C++ preprocessor

This is a simple C/C++ preprocessor.

The goal is to have good conformance with the C and C++ standards and to handle nonstandard preprocessor extensions in gcc / clang / visual studio preprocessors. Most of the preprocessor testcases in gcc and clang are handled OK by simplecpp.

To see how you can use simplecpp in your project, you can look at the file main.cpp.

Simplecpp has better fidelity than normal C/C++ preprocessors.
 * Preprocessor directives are available.
 * Comments are available.
 * Tracking macro usage.

This information is normally lost during preprocessing but it can be necessary for proper static analysis.

## Status
![CI-windows](https://github.com/danmar/simplecpp/workflows/CI-windows/badge.svg)
![CI Unixish](https://github.com/danmar/simplecpp/workflows/CI%20Unixish/badge.svg)


## Compiling

Compiling standalone simplecpp preprocessor:

Either:

    g++ -o simplecpp main.cpp simplecpp.cpp

Or:

    make


Compiling and running tests (you need python to run the gcc/clang test cases)

    make test

