.. RVL System documentation master file, created by
   sphinx-quickstart on Sat Jul 10 10:45:16 2021.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.

Welcome to the RVL System documentation
=======================================

RVL System is a suite of tools and systems for controlling lighting setups. The
primary focus is LED strips used in maker circles, such as `WS2812B`_ strips.
This project is designed to be usable off-the-shelf *and* to be extended and
integrated into custom solutions.

RVL System is composed of the following six pieces:

.. toctree::
   :maxdepth: 1

   RVL Controller Board <controller-board/index>
   RVL Firmware <firmware/index>
   Home Lights <home-lights/index>
   RVL Library <rvl/index>
   RVL Arduino WiFi Plugin <rvl-arduino-wifi/index>
   RVL Node.js Plugin <rvl-node/index>

The first three are designed to be used off the shelf, and are built on top of
the latter three. The latter three are reusable libraries that can be integrated
into other projects for more custom solutions.

1. RVL Controller Board
-----------------------

The RVL Controller Board is an ESP32 based piece of hardware that's somewhere
between a general purpose development board, and a special purpose LED
controller.

2. RVL Firmware
---------------

The RVL Controller Board comes with default firmware that allows you to connect
an LED strip to it and start showing animations without any programming. In
addition, multiple boards can sycnhronize with each other over WiFi to show the
same animation. This firmware is written to run on the ESP32 and ESP8266. It's
written using the Arduino framework, so is straightforward to get working on
other boards with similar or better capabilities that also support the Arduino
framework.

3. Home Lights
---------------

Home Lights is a web server designed to be run on a Raspberry Pi or other
computing platform that runs full time in a home. This app provides an easy to
use interface for controlling lights in a home setting. In addition to
controlling RVL Controller Boards, Home Lights can also control Philips Hue and
LIFX smart bulbs.

4. RVL Library
--------------

RVL Firmware and Home Lights both rely on the core RVL Library to manage
communication and synchronization. This library is written in generic C++11 and
doesn't rely on any external libraries or platform specific runtimes. This way,
the RVL Library can be compiled in any C++ environment. In order to connect this
library to a specific communication protocol/stack, it needs a platform plugin,
such as RVL Arduino WiFi or RVL Node.

5. RVL Arduino WiFi
-------------------

RVL Arduino WiFi is a C++ based platform plugin for the RVL Library that
provides support for RVL to run on an Arduino compatible board and synchronizes
over WiFi via UDP.

6. RVL Node
-----------

RVL Node is a C++/WASM/JavaScript based platform plugin that provides support
for RVL to run in Node.js and synchronizes over UDP (i.e. WiFi, Ethernet, etc.).
RVL Node can only act in controller mode, and cannot control an LED strip
directly.

.. _WS2812B: https://cdn-shop.adafruit.com/datasheets/WS2812B.pdf
