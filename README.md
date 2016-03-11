Bestericoin integration/staging tree
================================

http://www.besteri.ru

Copyright (c) 2009-2013 Bitcoin Developers
Copyright (c) 2013-2014 DarkCoin Developers
Copyright (c) 2016 Bestericoin Developers

What is Bestericoin?
----------------

Bestericoin uses a modified version of the bitcoin and darkcoin protocol.  The protocol was selected for energy efficiency reasons.  Internal testing indicated energy savings of between 30-50% compared to the litecoin algorithm.

The bitcoin hashing algorithm was avoided due to the perceived centralisation of bitcoin transaction processing in large data centres.  The technology involved has evolved into specialised integrated circuits that only deep pocket investors are able to invest and reap large profits.  The tendency towards centralisation is viewed as a potential weakness.  Should governments try to control bitcoin, it would be relatively easy to direct a small number of data centres to operate an approved version of the bitcoin protocol.  Enforcing protocol change across a highly decentralised network of computers would be more difficult.

For the above reasons, the X11 algorithm was selected to provide adequate diversification in transaction processing whilst mitigating the issue of botnet attacks if a pure CPU only hashing algorithm was selected.

Protocol specifics
------------------

Hashing algorithm: X11 
Block reward: 100 bestericoins per block, constant
Block generation: 2.5 minutes
Difficulty re-targets: DGW ver 2.0
Total bestericoins: 23 Billion bestericoins over 80 years
https://github.com/Besteri/bestericoin.git

For more information, as well as an immediately useable, binary version of
the Bestericoin client sofware, see http://www.besteri.ru.

License
-------

Bestericoin is released under the terms of the MIT license. See `COPYING` for more
information or see http://opensource.org/licenses/MIT.

Development process
-------------------

Developers work in their own trees, then submit pull requests when they think
their feature or bug fix is ready.

If it is a simple/trivial/non-controversial change, then one of the Bestericoin
development team members simply pulls it.

If it is a *more complicated or potentially controversial* change, then the patch
submitter will be asked to start a discussion (if they haven't already) on the
[mailing list](http://sourceforge.net/mailarchive/forum.php?forum_name=bitcoin-development).

The patch will be accepted if there is broad consensus that it is a good thing.
Developers should expect to rework and resubmit patches if the code doesn't
match the project's coding conventions (see `doc/coding.txt`) or are
controversial.

The `master` branch is regularly built and tested, but is not guaranteed to be
completely stable. [Tags](https://github.com/bitcoin/bitcoin/tags) are created
regularly to indicate new official, stable release versions of Bestericoin.

Testing
-------

Testing and code review is the bottleneck for development; we get more pull
requests than we can review and test. Please be patient and help out, and
remember this is a security-critical project where any mistake might cost people
lots of money.

### Automated Testing

Developers are strongly encouraged to write unit tests for new code, and to
submit new unit tests for old code.

Unit tests for the core code are in `src/test/`. To compile and run them:

    cd src; make -f makefile.unix test

Unit tests for the GUI code are in `src/qt/test/`. To compile and run them:

    qmake BITCOIN_QT_TEST=1 -o Makefile.test bitcoin-qt.pro
    make -f Makefile.test
    ./bestericoin-qt_test

