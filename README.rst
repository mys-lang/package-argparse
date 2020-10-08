|buildstatus|_

Argparse
========

A command line argument parser in the `Mys programming language`_.

Examples
========

.. code-block:: python

   from argparse import Parser

   def main(argv: [string]):
       parser = Parser("tar")
       parser.add_option("--verbose",
                         short="-v",
                         multiple_occurrences=True,
                         help="Verbose output.")
       parser.add_positional("file",
                             help="A file.")

       args = parser.parse(argv)

       print(args)

.. |buildstatus| image:: https://travis-ci.com/eerimoq/mys-argparse.svg?branch=master
.. _buildstatus: https://travis-ci.com/eerimoq/mys-argparse

.. _Mys programming language: https://github.com/eerimoq/mys
