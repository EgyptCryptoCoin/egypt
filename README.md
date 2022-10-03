Egypt Core integration/staging tree
=====================================

https://egyptegy.com

What is Egypt?
----------------

Egypt is an experimental digital currency that enables instant payments to
anyone, anywhere in the world. Egypt uses peer-to-peer technology to operate
with no central authority: managing transactions and issuing money are carried
out collectively by the network. Egypt Core is the name of open source
software which enables the use of this currency.

For more information, as well as an immediately useable, binary version of
the Egypt Core software, see [https://github.com/EgyptCryptoCoin/egypt.git).

Build and compile
-----------------
-- Server must be Ubuntu 18.04 LTS x64

Mining
------
-- in /root type those commands >>>

sudo apt-get install libcurl4-openssl-dev libncurses5-dev pkg-config automake yasm

git clone https://github.com/pooler/cpuminer.git

cd cpuminer

./autogen.sh

./configure CFLAGS="-O3"

make

-- You can get your EGY wallet address by downloading the wallet through that link >>>

https://github.com/EgyptCryptoCoin/Egypt-WebWallet/raw/main/egypt-qt.exe

-- after install type the fooling >>>

./minerd --url=127.0.0.1:5775 --user=coinuser --pass=coinpassword --coinbase-addr=(Your EGY wallet address)

License
-------

Egypt Core is released under the terms of the MIT license. See [COPYING](COPYING) for more
information or see https://opensource.org/licenses/MIT.

Development Process
-------------------

The `master` branch is regularly built and tested, but is not guaranteed to be
completely stable. [Tags](https://github.com/egypt-project/egypt/tags) are created
regularly to indicate new official, stable release versions of Egypt Core.

The contribution workflow is described in [CONTRIBUTING.md](CONTRIBUTING.md).

The developer [mailing list](https://egyptegy.com)
should be used to discuss complicated or controversial changes before working
on a patch set.

Developer IRC can be found on Freenode at #egypt-dev.

### Automated Testing

Developers are strongly encouraged to write [unit tests](src/test/README.md) for new code, and to
submit new unit tests for old code. Unit tests can be compiled and run
(assuming they weren't disabled in configure) with: `make check`. Further details on running
and extending unit tests can be found in [/src/test/README.md](/src/test/README.md).

There are also [regression and integration tests](/qa) of the RPC interface, written
in Python, that are run automatically on the build server.
These tests can be run (if the [test dependencies](/qa) are installed) with: `qa/pull-tester/rpc-tests.py`

The Travis CI system makes sure that every pull request is built for Windows, Linux, and OS X, and that unit/sanity tests are run automatically.

### Manual Quality Assurance (QA) Testing

Changes should be tested by somebody other than the developer who wrote the
code. This is especially important for large or high-risk changes. It is useful
to add a test plan to the pull request description if testing the changes is
not straightforward.

# Egypt EGY
