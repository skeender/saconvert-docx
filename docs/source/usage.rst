Usage
=====

.. _installation:

Installation
------------

To use saconvert, first install it using pip:

.. code-block:: console

   pip3 install saconvert

Converting | Length
----------------

SAconvert has many converting options. In this case, we will use 
the LengthConverter. You can use the ``LengthConverter`` class to
specify the unit you want to convert from:

.. autofunction:: LengthConverter

There are 2 parameters for the ``LengthConverter`` class. The ``value`` parameter should be a
float (a whole number or a decimal number) specifying how many of those units you want to convert to. 
Otherwise, :py:func:`LengthConverter`will return an error. The ``unit`` parameter should be a string.
It will specify the unit name you want to convert from. The current units supported are:
- ``Meter``
- ``Kilometer``
- ``Centimeter``
- ``Millimeter``
- ``Micrometer``
- ``Nanometer``
- ``Mile``
- ``Yard``
- ``Foot``
- ``Inch``
- ``Light Year``
Make sure the first letter of the unit is capitalized as shown above.
If not, it will return a ValueError. Here is an example of how you should
define the unit(s) you want to convert from:
>>> LengthConverter(1, "Yard")

Converting to another unit is simple. Just add a function to it.
Here is a list of the examples of all the units you 
can convert to:

- ``to_meter()``
- ``to_kilometer()``
- ``to_centimeter()``
- ``to_millimeter()``
- ``to_micrometer()``
- ``to_nanometer()``
- ``to_mile()``
- ``to_yard()``
- ``to_foot()``
- ``to_inch()``
- ``to_light_year()``

Here is an example to convert a unit to another:
>>> LengthConverter(1, "Yard").to_inch()

Here is the final code on how to use LengthConverter:

.. code-block:: console

   pip3 install saconvert

.. code-block:: python

   from saconvert import LengthConverter

   converter = LengthConverter(1, "Foot")
   print("1 foot is equal to " + converter.to_inch() + " inches.")

This will print out:

.. code-block:: console

   1 foot is equal to 12 inches.
