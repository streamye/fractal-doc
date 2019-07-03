Download Instructions for Mac OS X
---------------------------------------

Download directly
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

There are two steps here , first download files ,second add files to executable path . See details below.

Step1
''''''
By far the easiest way to use go-fractal is to download directly.There is a zip file including four kind of files,you can download `here  <./_static/mac_file/fractal.zip>`_:
Four files are:

- 1. main executable file ``gftl`` , used for startting a node. 
- 2. tool file ``gtool``,used for account management etc...
- 3. wasm lib file ``lib`` , a virtual machine lib.
- 4. main chain config file ``test.toml``, you need to use it when you start node.
- 5. wasmtest file executable ``wasmtest``, for smart contract use.

Step2
''''''
To use all these executable files , you need to add file path to system path.
::
    // change to current user directory 
    $ cd ~

    $ vim ~/.bash_profile
    change path ,add export PATH: 
    export PATH=filePath:$PATH

    //make PATH work
    $ source ~/.bash_profile 
**WARNING** if your gftl and gtool executable files lies in /Users/jimi/fractal ,then filePath is /Users/jimi/fractal.

