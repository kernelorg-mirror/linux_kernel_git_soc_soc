====================
Kernel driver lp3944
====================

  * National Semiconductor LP3944 Fun-light Chip

    Prefix: 'lp3944'

    Addresses scanned: None (see the Notes section below)

    Datasheet:

	Publicly available at the National Semiconductor website
	http://www.national.com/pf/LP/LP3944.html

Authors:
	Antonio Ospite <ospite@studenti.unina.it>


Description
-----------
The LP3944 is a helper chip that can drive up to 8 leds, with two programmable
DIM modes; it could even be used as a gpio expander but this driver assumes it
is used as a led controller.

The DIM modes are used to set _blink_ patterns for leds, the pattern is
specified supplying two parameters:

  - period:
	from 0s to 1.6s
  - duty cycle:
	percentage of the period the led is on, from 0 to 100

Setting a led in DIM0 or DIM1 mode makes it blink according to the pattern.
See the datasheet for details.

LP3944 can be found on Motorola A910 smartphone, where it drives the rgb
leds, the camera flash light and the lcds power.
