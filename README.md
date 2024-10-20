## Standalone Bitcoin Consensus Engine

This repository contains the historical bitcoin consensus Engine
exposed in an experimental standalone binary, i.e `bitcoin-chainstate`.This
is a fork of the libbitcoinkernel project from its 27.0 release tag,
with the bugs fixes in the build system to *actually* make it works.

This can be experimented with the following commands:

```
autogen.sh
configure --enable-reduce-exports --enable-experimental-util-chainstate \
    --with-experimental-kernel-lib --enabled-shared
make src/bitcoin-chainstate

./src/bitcoin-chainstate

Usage: ./src/bitcoin-chainstate DATADIR
Display DATADIR information, and process hex-encoded blocks on standard input.

IMPORTANT: THIS EXECUTABLE IS EXPERIMENTAL, FOR TESTING ONLY, AND EXPECTED TO
           BREAK IN FUTURE VERSIONS. DO NOT USE ON YOUR ACTUAL DATADIR.


```

For more information about the libbitcoinkernel project, see this [blog article](https://laanwj.github.io/2021/01/21/decentralize.html)

This a very experimental project, so please do not use it in production
to handle real bitcoin flows or real money.

This repository is for read-only and only for developers skilled in
bitcoin engineering wishing to re-write a consensus-compatible full-node
or another component of the bitcoin stack, in whatever language they
wish (go, c++, haskell, python, etc), without precisly having to re-write
a consensus engine, bug for bug, themselves. Skills in C / C++ is still
strongly recommended.

This repository does not accept code contributions at the time. Issues
and PRs will be closed without motivations.
