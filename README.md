Snap Framework
==============

This is the first developer prerelease of the Snap Framework snap
tool.  For more information about Snap, read the `README.SNAP.md` or
visit the Snap project website at http://www.snapframework.com/.

Snap is a nascent web framework for Haskell, based on iteratee I/O (as
[popularized by Oleg
Kiselyov](http://okmij.org/ftp/Streams.html#iteratee)).


## Library contents

This is the `snap` executable and supporting library, which contains:

  * a command-line utility for creating initial Snap applications

  * a library allowing Snap applications to recompile actions on the
    fly in development mode, with no performance loss in production
    mode.


Building snap
=============

The snap tool and library are built using
 [Cabal](http://www.haskell.org/cabal/) and
[Hackage](http://hackage.haskell.org/packages/hackage.html). Just run

    cabal install

from the `snap` toplevel directory.


## Building the Haddock Documentation

The haddock documentation can be built using the supplied `haddock.sh` shell
script:

    ./haddock.sh

The docs get put in `dist/doc/html/`.


## Building the testsuite

Snap is still in its very early stages, so most of the "action" (and a big
chunk of the code) right now is centred on the test suite. Snap aims for 100%
test coverage, and we're trying hard to stick to that.

To build the test suite, `cd` into the `test/` directory and run

    $ cabal configure
    $ cabal build

From here you can invoke the testsuite by running:

    $ ./runTestsAndCoverage.sh


The testsuite generates an `hpc` test coverage report in `test/dist/hpc`.
