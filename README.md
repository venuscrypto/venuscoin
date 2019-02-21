Venuscoin integration/staging tree
================================

https://venuscrypto.org/

Copyright (c) 2009-2014 Bitcoin Developers
Copyright (c) 2011-2014 Litecoin Developers
Copyright (c) 2016-2018 Venuscoin Developers

What is Venuscoin?
----------------

Venuscoin is a lite version of Bitcoin using scrypt as a proof-of-work algorithm.
 - 30 second block targets
 - ~27 million total coins

The rest is the same as Bitcoin.
 - 50 coins per block

For more information please visit, https://venuscryto.org/

License
-------

Venuscoin is released under the terms of the MIT license. See `COPYING` for more
information or see http://opensource.org/licenses/MIT.

PORTS
------
mainnet - 17000     
testnet - 17001     
    
rpc - 17002     
rpc testnet - 17003     

API Call List    
--------------
https://en.bitcoin.it/wiki/Original_Bitcoin_client/API_calls_list    

    
Development process
-------------------

Developers work in their own trees, then submit pull requests when they think
their feature or bug fix is ready.

If it is a simple/trivial/non-controversial change, then one of the Venuscoin
development team members simply pulls it.

If it is a *more complicated or potentially controversial* change, then the patch
submitter will be asked to start a discussion with the devs and community.

The patch will be accepted if there is broad consensus that it is a good thing.
Developers should expect to rework and resubmit patches if the code doesn't
match the project's coding conventions (see `doc/coding.txt`) or are
controversial.

The `master` branch is regularly built and tested, but is not guaranteed to be
completely stable. [Tags](https://github.com/venuscoin-project/venuscoin/tags) are created
regularly to indicate new official, stable release versions of Venuscoin.

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
    ./venuscoin-qt_test

DEPENDENCIES
------------
sudo apt-get install build-essential libtool autotools-dev autoconf pkg-config libssl-dev   
sudo apt-get install libboost-all-dev   
sudo add-apt-repository ppa:bitcoin/bitcoin     
sudo apt-get update     
sudo apt-get install libminiupnpc-dev    
    
sudo apt-get install libdb4.8-dev   
sudo apt-get install libdb4.8++-dev     
sudo apt-get install libboost1.37-dev (If using Boost 1.37, append -mt to the boost libraries in the makefile)      
sudo apt-get install libssl1.0-dev      
sudo apt-get install libdb++-dev    

COMPILE WITHOUT UPNP
--------------------
make -f makefile.unix USE_UPNP=-
