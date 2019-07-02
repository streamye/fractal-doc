Download Instructions for Mac OS X
---------------------------------------

First Method:   Download directly
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Step1
''''''
By far the easiest way to use go-fractal is to download directly.There is a zip file including four kinds of files,you can download `gftl  <./_static/mac_file/fractal.zip>`_:
Four files are:

- 1. main executable file ``gftl`` . 
- 2. tool file ``gtool``.
- 3. wasm lib file ``lib`` .
- 4. main chain config file ``test.toml``.

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

