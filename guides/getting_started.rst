Getting Started
=================

**Chapter 1**

Let’s start your fractal journey! In this chapter, we’ll discuss:

- Installing fractal on macOS and Linux (Centos,Ubuntu)
- Getting your first block 
- More about ``start_private.sh``

Installation
--------------
Here we provide macOs and Linux (Centos,Ubuntu) versions. You can download here:

Download
''''''''''

- `macOS download  <../_static/mac_file/gftl.macos.v0.1.0.tar.gz>`_
- `ubuntu download  <../_static/ubuntu_file/gftl.ubuntu.v0.1.0.tar.gz>`_
- `centos download  <../_static/centos_file/gftl.centos.v0.1.0.tar.gz>`_


 | **Command Line Notation**
 | In this chapter and throughout the book, we’ll show some commands used in the terminal. 
 | Lines that you should enter in a terminal all start with $. You don’t need to type in the $ character; it indicates the start of each command. Lines that don’t start with $ typically show the output of the previous command. 
 | ``//`` is comment, don't copy words after that.

Start Node
'''''''''''''
After you download files, you need to decompress and run it. Here we take macOS as example.

1.If you want to start a ``Private-Network``

step 1: decompress file to current directory 

.. code-block:: bash 

    $ tar -zxvf gftl.macos.v0.1.0.tar.gz  -C .   

step 2: enter gftl.macos.v0.1.0

.. code-block:: bash 

    $ cd gftl.macos.v0.1.0   

step 3: make it executable 

.. code-block:: bash 

    $ chmod +x start_private.sh 

step 4: start node

.. code-block:: bash 

    $ ./start_private.sh 


2.If you want to start a ``TestNetwork``:

step 1: decompress file to current directory 

.. code-block:: bash 

    $ tar -zxvf gftl.macos.v0.1.0.tar.gz  -C .   

step 2: enter gftl.macos.v0.1.0

.. code-block:: bash 

    $ cd gftl.macos.v0.1.0   

step 3: make it executable 

.. code-block:: bash 

    $ chmod +x start.sh 
    
step 4: start node

.. code-block:: bash 

    $ ./start.sh 

**NOTE: If you want to start mining for yourself, go on reading, otherwise you can stop here.**

step 5: create account in wallet, go to `fractal wallet <xxxx>`_ to see how to create account.

step 6: request balance from fractal, go to `fractal explorer <xxxx>`_ to see how to request balance.

step 7: set mining coinbase to local node, go to `fractal wallet <xxxx>`_ to see how to set coinbase.

| **NOTE**
|  The main difference between ``Private-Network`` and ``TestNetwork`` is that you have to get balance from ``Testnetwork`` if you want to start-mining,
|  while in ``Private-Testnetwork`` you can allocate balance for yourself.
|  For simple use, you can just start a ``Private-Network`` as starter.After building ``Private-Network``,building  ``Testnetwork`` will be very simple.
|

If you want to look through details of each shell script ,go to `How to Guide <how_to_guide.html>`_ for more information.

Getting your first block 
---------------------------

It’s traditional when learning a new language to write a little program that prints the text **Hello, world!** to the screen.
Here we get our newest block back to indicate fractal node is working well:

.. code-block:: bash 

    $ ./start_private.sh check
    {"jsonrpc":"2.0","id":"1","result":{"Body":{"transactions":[],"txpackages":[]},"FullHash":"0x85eadcda32d8b4eab5ffabe588d4eba970c48a23e3f5b88c3233cd637f2bf15a","Header":{"parentHash":"0x0000000000000000000000000000000000000000000000000000000000000000","round":1560324859,"sig":"AA==","miner":"0x0000000000000000000000000000000000000000","difficulty":5000000000000000,"height":0,"amount":1,"stateHash":"0x91fd53918ab0267bf0f1a12e59c04c8892b9c49028baaab146c2ea39bd98bdb1","txHash":"0x0000000000000000000000000000000000000000000000000000000000000000","receiptsRoot":"0x0000000000000000000000000000000000000000000000000000000000000000","parentFullHash":"0x0000000000000000000000000000000000000000000000000000000000000000","logsBloom":"0x00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000","confirms":[],"fullSig":"","minedTime":0,"hopCount":0},"SimpleHash":"0x60428333471c87045da921fc326ee2846ac607a83a05ce0f0a03d7fb158cb5ae"}}

**WARNING** On ubuntu you may find ``curl`` is not installed: ``curl: command not found``, run ``sudo apt-get install curl`` to install it.

More about **start_private.sh**
---------------------------
We have used ``start_private.sh`` or ``start.sh`` for several times, now we explain ``start_private.sh`` in detail, ``start.sh`` is the same:

1. start fractal node: use this command if you want to start fractal node; when you shut down your PC ,you can run this to get fractal node run again

.. code-block:: bash 

    $ ./start_private.sh

2. clean files: this command deletes all files to restore the original files state

.. code-block:: bash 

    $ ./start_private.sh del


3. check: this command checks whether the fractal node runs well

.. code-block:: bash 

    $ ./start_private.sh check


4. stop: it stops fractal node, shut it down

.. code-block:: bash 

    $ ./start_private.sh stop


