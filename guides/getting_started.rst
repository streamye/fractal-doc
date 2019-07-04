Getting Started
=================

Let’s start your fractal journey! In this chapter, we’ll discuss:

- Installing fractal on Linux, macOS, and Centos
- Getting your first block 
- More about ``start_self.sh``

Installation
--------------
Here we provide macOs and Linux versions. You can download here:

Download
''''''''''

- `macOS download  <../_static/mac_file/gftl.macos.v0.1.0.zip>`_
- `Linux download  <../_static/mac_file/gftl.macos.v0.1.0.zip>`_

After downloading .........

| **Command Line Notation**
| In this chapter and throughout the book, we’ll show some commands used in the terminal. 
| Lines that you should enter in a terminal all start with $. You don’t need to type in the $ character; 
| it indicates the start of each command. Lines that don’t start with $ typically show the output of the previous command. 
|

Start Node
'''''''''''''
If you want to start a ``Private-Testnetwork``
::
    1. unzip it
    2. $ chmod +x start_self.sh //to make it executable 
    3. $ ./start_self.sh


2.If you want to start a ``Testnetwork``:
::
    1. unzip it
    2. $ chmod +x start.sh //to make it executable 
    3. $ ./start.sh

| **NOTE**
|  The main difference between ``Private-Testnetwork`` and ``Testnetwork`` is that you have to get balance from ``Testnetwork`` if you want to start-mining,
|  while in ``Private-Testnetwork`` you can allocate balance for yourself.
|  For simple use, you can just start a ``Private-Testnetwork`` as starter.After building ``Private-Testnetwork``,building  ``Testnetwork`` will be very simple.
|

If you want to lookup details of each shell script ,go `How to Guide <how_to_guide.html>`_.

Getting your first block 
---------------------------
 It’s traditional when learning a new language to write a little program that prints the text **Hello, world!** to the screen.
 Here we get our first block with height 0:
 ::
    $ ./start_self.sh check
    {"jsonrpc":"2.0","id":"1","result":{"Body":{"transactions":[],"txpackages":[]},"FullHash":"0x85eadcda32d8b4eab5ffabe588d4eba970c48a23e3f5b88c3233cd637f2bf15a","Header":{"parentHash":"0x0000000000000000000000000000000000000000000000000000000000000000","round":1560324859,"sig":"AA==","miner":"0x0000000000000000000000000000000000000000","difficulty":5000000000000000,"height":0,"amount":1,"stateHash":"0x91fd53918ab0267bf0f1a12e59c04c8892b9c49028baaab146c2ea39bd98bdb1","txHash":"0x0000000000000000000000000000000000000000000000000000000000000000","receiptsRoot":"0x0000000000000000000000000000000000000000000000000000000000000000","parentFullHash":"0x0000000000000000000000000000000000000000000000000000000000000000","logsBloom":"0x00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000","confirms":[],"fullSig":"","minedTime":0,"hopCount":0},"SimpleHash":"0x60428333471c87045da921fc326ee2846ac607a83a05ce0f0a03d7fb158cb5ae"}}


More about ``start_self.sh``
---------------------------
We have used ``start_self.sh`` or ``start.sh`` for several times,now we explain ``start_self.sh`` in detail,``start.sh`` is the same:
::
    $ ./start_self.sh  // start fractal node , if you shut down your PC ,you can run this to get fractal node run again
    $ ./start_self.sh del // it deletes all files to restore the original state
    $ ./start_self.sh check // it check if the fractal node runs well
    $ ./start_self.sh stop  // it stops fractal node ,shut it down

