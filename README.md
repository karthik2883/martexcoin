MarteX [MXT] integration/staging tree
=====================================

http://www.martexcoin.org

What is the MarteX [MXT] Blockchain?
---------------------------

The MarteX [MXT] Blockchain is an experimental smart contract platform protocol that enables 
instant payments to anyone, anywhere in the world in a private, secure manner. 
MarteX [MXT] uses peer-to-peer blockchain technology developed by Bitcoin to operate
with no central authority: managing transactions, execution of contracts, and 
issuing money are carried out collectively by the network. MarteX [MXT] is the name of 
open source software which enables the use of this protocol.

Specifications and General info
------------------
MarteX uses libsecp256k1,
			  libgmp,
			  Boost1.63,
			  OR Boost1.57,  
			  Openssl1.02k,
			  Berkeley DB 6.2.23,
			  QT5.8 to compile


Block Spacing: 1 Minutes
Stake Minimum Age: 15 Confirmations (PoS-v3) | 30 Minutes (PoS-v2)

Port: 51315
RPC Port: 51314


BUILD LINUX
-----------
1) git clone https://github.com/martexcoin/martexcoin

2) cd martexcoin/src

3) sudo make -f makefile.unix            # Headless

(optional)

4) strip MarteXd

5) sudo cp MarteXd /usr/local/bin

License
-------

MarteX [MXT] is released under the terms of the MIT license. See [COPYING](COPYING) for more
information or see https://opensource.org/licenses/MIT.

Development Process
-------------------

The `master` branch is regularly built and tested, but is not guaranteed to be
completely stable. [Tags](https://github.com/martexcoin/martexcoin/tags) are created
regularly to indicate new official, stable release versions of MarteX [MXT].

The contribution workflow is described in [CONTRIBUTING.md](CONTRIBUTING.md).

The developer [mailing list](https://lists.linuxfoundation.org/mailman/listinfo/bitcoin-dev)
should be used to discuss complicated or controversial changes before working
on a patch set.

Developer Slack can be found at http://martexcoin.slack.com.

Testing
-------

Testing and code review is the bottleneck for development; we get more pull
requests than we can review and test on short notice. Please be patient and help out by testing
other people's pull requests, and remember this is a security-critical project where any mistake might cost people
lots of money.

### Automated Testing

Developers are strongly encouraged to write [unit tests](/doc/unit-tests.md) for new code, and to
submit new unit tests for old code. Unit tests can be compiled and run
(assuming they weren't disabled in configure) with: `make check`

There are also [regression and integration tests](/qa) of the RPC interface, written
in Python, that are run automatically on the build server.

### Manual Quality Assurance (QA) Testing

Changes should be tested by somebody other than the developer who wrote the
code. This is especially important for large or high-risk changes. It is useful
to add a test plan to the pull request description if testing the changes is
not straightforward.
