A subcommand example
====================

``--verbose`` before subcommand:

.. code-block:: text

   $ mys run -- -vv write 0 beac1d
   ...
   Number of --verbose:  2
   Address:              0
   Data:                 beac1d
   Erase?:               False

``--verbose`` after subcommand also works:

.. code-block:: text

   $ mys run -- write 0 beac1d -v
   ...
   Number of --verbose:  1
   Address:              0
   Data:                 beac1d
   Erase?:               False
