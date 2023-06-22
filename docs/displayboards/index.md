# Displayboards

## General

We currently support the following display boards, not all of them support all operating modes: 

* FDS MLED
* ALGE-Timing D-Line
* Videowall/LED screens (via [dbnetsoft.Screens software](https://www.dbnetsoft.com/product/screens/))

## Setup

In the `Displayboards Control` view, click on Add Displayboard to add a new displayboard and select the type of display. You can drive more than one board at once and going out on different COM-Ports for different displays. 

For ALGE display boards, it is not possible to output to several addresses on one COM port at the moment. You need one COM-Port per address.

!!! warning

    Please make sure to have an exporter set up as indicated [here](../home/configuration/index.md). Otherwise this module will not receive passings in real-time and can act upon them. If you plan on only using runtimes, clocks or texts you can ignore this configuration.
