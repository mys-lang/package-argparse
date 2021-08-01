|discord|_
|test|_
|stars|_

About
=====

A command line argument parser in the `Mys programming language`_.

Project: https://github.com/mys-lang/package-argparse

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

       print("File:                ", args.value_of("file"))
       print("Number of --verbose: ", args.occurrences_of("--verbose"))

Build and run:

.. code-block:: myscon

   ❯ mys run -- --verbose foobar.txt
    ✔ Reading package configuration (0 seconds)
    ✔ Building (0.01 seconds)
   File:                 foobar.txt
   Number of --verbose:  1

Show help:

.. code-block:: myscon

   ❯ mys run -- --help
    ✔ Reading package configuration (0 seconds)
    ✔ Building (0.01 seconds)
   Usage: tar ...

   Options:

     -h, --help Show this help.
     -v, --verbose Verbose output.

   Positionals:

     file A file.

API
===

.. mysfile:: src/lib.mys

.. |discord| image:: https://img.shields.io/discord/777073391320170507?label=Discord&logo=discord&logoColor=white
.. _discord: https://discord.gg/GFDN7JvWKS

.. |test| image:: https://github.com/mys-lang/package-argparse/actions/workflows/pythonpackage.yml/badge.svg
.. _test: https://github.com/mys-lang/package-argparse/actions/workflows/pythonpackage.yml

.. |stars| image:: https://img.shields.io/github/stars/mys-lang/package-argparse?style=social
.. _stars: https://github.com/mys-lang/package-argparse

.. _Mys programming language: https://mys-lang.org
