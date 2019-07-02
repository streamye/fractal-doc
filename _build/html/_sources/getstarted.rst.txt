Hello World!
------------


Create a new directory called "hello" in the contracts  directory you previously created, or through your     system GUI or with cli and enter the directory.

.. code-block:: C 

    cd CONTRACTS_DIR
    mkdir hello
    cd hello

Create a new file, "hello.cpp" and open it in your favourite editor.

.. code-block:: C 

    touch hello.cpp

Below the ``fractal.hpp`` header file is included. The eosio.hpp file includes a few classes required to write a smart contract.

.. code-block:: C 

    #include <fractal/fractal.hpp>

Using the eosio namespace will reduce clutter in your code. For example, by setting ``using namespace fractal``;, ``fractal::print("foo")`` can be written print("foo")

.. code-block:: C 

    using namespace fractal;

Create a standard C++11 class. The contract class needs to extend ``fractal::contract`` class which is included earlier from the ``fractal.hpp`` header

.. code-block:: C

    #include <fractal/fractal.hpp>

    using namespace fractal;

    class [[fractal::contract]] hello : public contract {};

An empty contract doesn't do much good. Add a public access specifier and a using-declaration. The ``using`` declaration will allow us to write more concise code.

.. code-block:: C

    #include < fractal/fractal.hpp>
 
    using namespace fractal;

    class [[fractal::contract]] hello : public contract {

      public:
	         using contract::contract;
    };

The above action accepts a parameter called ``user`` that's a ``std:string type``. FRACTAL comes with a number of typedefs. Using the ``fractal::print`` library previously included, concatenate a string and print the ``user parameter``.

As is, the ABI GLOSSARY:ABI generator in ``fractal.cdt`` won't know about the hi() action without an attribute. Add a C++11 style attribute above the action, this way the abi generator can produce more reliable output.

.. code-block:: C

    #include <fractal/fractal.hpp>

    using namespace fractal;

    class [[fractal::contract]] hello : public contract {
      public:
          using contract::contract;

          [[fractal::action]]
          void hi( std::string user ) {
             print( "Hello, ", user);
          }
    };

Everything together, here's the completed hello world contract

.. code-block:: C

    #include <fractal/fractal.hpp>

    using namespace fractal;

    class [[fractal::contract]] hello : public contract {
      public:
          using contract::contract;

          [[fractal::action]]
          void hi( std::string user ) {
             print( "Hello, ", user);
          }
    };

You can compile your code to web assembly (.wasm) as follows:

.. code-block:: C

    fractal-cpp -abigen -o hello.wasm hello.cpp

Above command generates two file hello.wasm and hello.abi. You can test the contract as follows:

.. code-block:: C

    wasmtest --wasm hello.wasm --abi hello.abi --action hi args "[]" exec



