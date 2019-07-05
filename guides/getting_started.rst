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

- `macOS download  <../_static/mac_file/gftl.macos.v0.1.0.zip>`_
- `Linux download  <../_static/mac_file/gftl.macos.v0.1.0.zip>`_


 | **Command Line Notation**
 | In this chapter and throughout the book, we’ll show some commands used in the terminal. 
 | Lines that you should enter in a terminal all start with $. You don’t need to type in the $ character; it indicates the start of each command. Lines that don’t start with $ typically show the output of the previous command. 
 | ``//`` is comment, don't copy words after that.

Start Node
'''''''''''''
After you download files, you need to decompress and run it. Here we take macOS as example.

1.If you want to start a ``Private-Network``

.. code-block:: bash 

    //decompress file to current directory 
    $ tar -zxvf gftl.macos.v0.1.0.tar.gz  -C .   

    //enter gftl.macos.v0.1.0
    $ cd gftl.macos.v0.1.0   

    //make it executable 
    $ chmod +x start_private.sh 

    //start node
    $ ./start_private.sh 


2.If you want to start a ``TestNetwork``:

.. code-block:: bash 

    //decompress file to current directory 
    $ tar -zxvf gftl.macos.v0.1.0.tar.gz  -C .   

    //enter gftl.macos.v0.1.0
    $ cd gftl.macos.v0.1.0   

    //make it executable 
    $ chmod +x start.sh 
    
    //start node
    $ ./start.sh 


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


More about **start_private.sh**
---------------------------
We have used ``start_private.sh`` or ``start.sh`` for several times, now we explain ``start_private.sh`` in detail, ``start.sh`` is the same:

1. start fractal node: use this command if you want to start fractal node; when you shut down your PC ,you can run this to get fractal node run again

.. code-block:: bash 

    $ ./start_self.sh

2. clean files: this command deletes all files to restore the original files state

.. code-block:: bash 

    $ ./start_self.sh del


3. check: this command checks whether the fractal node runs well

.. code-block:: bash 

    $ ./start_self.sh check


4. stop: it stops fractal node, shut it down

.. code-block:: bash 

    $ ./start_self.sh stop


