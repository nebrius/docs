.. RVL System documentation master file, created by
   sphinx-quickstart on Sat Jul 10 10:45:16 2021.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.

Welcome to RVL System's documentation!
======================================

- One

  - One.One
  - One.Two

- Two

And here's a quoted paragraph
  I'm quoted!

This is a typical paragraph.  An indented literal block follows.

.. code-block:: cpp

   void main() {
      int foo = 10;
   }

This text has returned to the indentation of the first paragraph,
is outside of the literal block, and is therefore treated as an
ordinary paragraph.

.. toctree::
   :maxdepth: 1
   :caption: Contents:

   Controller Board <controller-board/index>
   Firmware <firmware/index>
   Home Lights <home-lights/index>

   RVL Library <rvl/index>
   RVL Arduino WiFi Plugin <rvl-arduino-wifi/index>
   RVL Node.js Plugin <rvl-node/index>

