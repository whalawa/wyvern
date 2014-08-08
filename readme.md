The Wyvern project
==================
The Wyvern programming language is a new language designed to smooth the use of internal DSLs in the form of type-specific languages.

Code examples can be found as part of our [testsuite](tools/src/wyvern/tools/tests/embedded), where TSL use can be seen in both TSL.test and parselang.test.

To run Wyvern, run bin/wyvern from the root directory after compiling, or run wyvern.tools.interpreter. No compilation target is currently avaliable.

Layout
-----------------
The tools directory contains the Wyvern compiler, the command line interface, and the supported tests.

From this point onwards, we refer to paths relative to ``./tools/src``.

The compiler itself is within ``wyvern/tools``, with most of its support files also contained within that directory.

The currently maintained examples of Wyvern are part of the Wyvern compiler test suite, in ``wyvern/tools/tests/embedded``. These tests use a DSL for each test, where each test is in a block of the form

```
  test [testname]([expected value]:[expected type])
    [test code]
```

``wyvern/tools/errors`` contains error reporting utility code.

``wyvern/tools/imports`` contains the various systems that resolve different types of imports.

``wyvern/tools/parsing`` contains the parser, as well as a number of AST elements that support parsing.

``wyvern/tools/typedAST`` contains the AST elements, which define both typechecking and interpreted evaluation.

``wyvern/tools/types`` contains the types that Wyvern uses.

``wyvern/tools/util`` contains a number of common utilities used by many of the other compiler elements.

Compilation
-----------------
Wyvern requires the Java 8 JDK.

It is strongly reccomended to use an IDE to compile Wyvern. Eclipse Kepler and IntelliJ 13 or up are supported. Please import the included project in tools/.project to do so.

Wyvern depends on a number of autogenerated files. Generating these files is the sole responsibillity of build.xml, and running this build is required before the compiler can be built.


License
---------------
See COPYING.TXT for the GPLv2 license under which this software is distributed.
