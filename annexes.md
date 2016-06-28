# Annex 1 - Compatibility of Experimental Activities with XO1.5HS (SKU121) and XO1.75 (SKU206)

The bulk of this work, in construction since the end of 2008, is based on Physics applications were extensively tested on XO1 with Measure Activity v31, 36 and 42, and TurtleBlocks Activity v109 and 130.

In principle, any other XO model can measure the same physical magnitudes; however not all of them perform equally for various reasons:

1. **All of them can measure Resistance correctly** when the aforementioned Activities include the particular model's calibration tables which must be previously tested.

2. **All of them can analyze sounds** in Measure Activity with base time and base frequency.

3. **All of them can synthesize sounds** of adjustable frequency (as was discussed).

**However the voltage readings won't be of the same quality** in different models because they have different impedance. In this sense, XO1 is the model that better approximates an ideal voltmeter (of infinite impedance).

## XO1.5HS (SKU121)

For those programs that measure resistance and voltage, do account for the difference in measuring ranges in relation to XO1 and modify them if appropriate.

All programs have been tested excepting:

* `24.Tabla RC.ta`
* `25.grafica V(V) t(s).ta`
* `36.Tabla LM35.ta`
* `37.termometro LM35.ta`
* `38.termofono LM35.ta`

## XO1.75 (SKU206)

At the time of finishing this work, this model consistently fails in the following way: when running any TB program it may measure the correct channel (generally CHL) or it will randomly return measurements coming from the other channel (CHR) (this error is generally known as *swapping*). This causes programs that measure volume, frequency, resistance and voltage to either function properly or not. Having made the query to the experts, we were informed that they were working on a solution involving low level modifications to the XO.

*The (interim) solution at the moment consists in working with TB from version 167 onwards and using an audio cable with the CHL and CHR cables joined with each other. This causes the loss of the ability to measure in double channel but in this regard XO1.75 should work like an XO1, as if reading CHL (monoaural).*

# Annex 2 - "Physics with XO" without XO

The deployment of Plan Ceibal in Uruguay began with the distribution of XO1 in primary school and XO1.5 in secondary school (except for Canelones department), then continued with the addition of standard netbooks which cannot apply most of the ideas present here.

Currently these netbooks have Ubuntu Linux installed including Audacity which allows analysis and synthesis of sounds (**see "10.4 Synthesis of sounds in other netbooks distributed by Plan Ceibal"**) and include Sugar allowing us to work with Measure and to write programs in TB using the built-in microphone and camera.

However, the Butiá team of the School of Engineering (UdelaR) has designed an (open hardware) board called **USB4butia** which is connected to the USB port and allows sensor measurements on any netbook. To work with it, the "TurtleBots" activity has been designed (http://activities.sugarlabs.org/es-ES/sugar/addon/4434).

Find more information about it at the following links:

http://www.fing.edu.uy/inco/proyectos/butia/mediawiki/index.php/P%C3%A1gina_principal

http://www.fing.edu.uy/inco/proyectos/butia/mediawiki/index.php/Usb4butia

With this excellent achievement the possibility has been opened to apply these ideas on any netbook available today. Around the end of 2012 I had the chance to make the first tests with said board and here I've summarized my first conclusions:

## Measurements of Voltage and Resistance

USB4butia is a board that exposes 6 ports which can be connected to sensors and actuators (not tested here). Its designers have produced "voltage sensor" and "resistance sensor" modules which can be directly connected to the male TRS 3.5mm audio cable based "Physics with XO" sensors.

Using their **Voltage Modules** we can read DC voltages between 0 and 4.99V. Using the **Resistance Modules** it's possible to read between 0Ω and some 7MΩ. The calibration levels (Turtlebots 18) for voltage and resistance (measured between 0Ω and 100kΩ) are very good.

The maximum sampling frequency, tested with a program that displayed a table of values **time/voltage1/voltage2** (dual channel measurement) is between 50 and 100 Hz. It varies with each program execution.

Input impedance as a voltmeter is in the order of 10 MΩ.

