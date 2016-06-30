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

# Annex 3 - Bibliography

- **Analog Devices (2003)**	http://www.datasheetcatalog.com/datasheets_pdf/A/D/1/8/AD1888.shtml Last accessed 03/02/13.
- **APFU** http://apfu.fisica.edu.uy/. Last accessed 03/02/13.
- **Bender (28/12/2011)** http://walterbender.org/?p=517. Last accessed 03/02/13.
- **Brito & Trinidad (2006)** BRITO, F. & TRINIDAD, G. (2006). Cronología Histórica de la Asociación de Profesores de Física del Uruguay (A.P.F.U.). Educación en Física (A.P.F.U.), Vol. 7, No 3, Setiembre de 2006.
- **BUTIÁ TORTUGA** http://www.fing.edu.uy/inco/cursos/fpr/wiki/index.php/Tutorial_Tortuga 
Last accessed 03/02/13.
- **ceibalJAM!** http://ceibaljam.org/drupal/?q=chuas Last accessed 03/02/13.
- **Correa & García (1991)** García, Pablo & Correa, Juan, (1991). DÉDALO: Interface para uso en experimentos de Física. Versión 1.0, Proyecto de apoyo al Laboratorio de Física del I.P.A., Montevideo, Uruguay: PEDECIBA, Documento sujeto a revisión
- **Chernuschi & Greco (1970)** Chernuschi & Greco (1970).  Teoría de errores de mediciones.  Buenos Aires, Argentina: Ed. EUDEBA.
- **Díaz & Pecard (1970)** Díaz, J. & Pecard, R. (1970). Física experimental para preparatorios (Tomo I). Montevideo, Uruguay: Ed. Kapelusz.
- **FLUKE 87** http://www.myflukestore.com/p1393/fluke_87-v.php Last accessed 03/02/13.
- **FORSTER** http://tonyforster.blogspot.com/2011/01/turtle-recursion.html 
Last accessed 03/02/13.
- **French (1974)** A. French (1974). Vibraciones y Onda. MIT, Barcelona: Ed. Reverté,
- **García (1991)** GARCÍA, P. (1991). Análisis Armónico de un sonido. Resumen Pedagógico, Año III, Nº6, Setiembre de 1991, (pág. 51-58))
- **Gil & Rodríguez (2001)** Gil, S. & Rodríguez, E. (2001). Física Re- Creativa. Experimentos de Física usando nuevas tecnologías. Bs. As., Argentina: Ed. Pearson Education.
- **Kay (1972)** http://www.mprove.de/diplom/gui/kay72.html. Last accessed 03/02/13.
- **Maiztegui & Gleiser (1980)** Maiztegui P. & Gleiser R. (1980). Introducción a las Mediciones de Laboratorio. Buenos Aires, Argentina: Ed. Kapelusz.
- **Maiztegui y otros (1987)** Maiztegui, A. y otros (1987). Física. Su enseñanza. Buenos Aires, Argentina: CONICET.
- **OLPC MEASURE** http://wiki.laptop.org/go/Measure/Hardware Last accessed 03/02/13.
- **OLPC News XO1.75** http://www.olpcnews.com/laptops/xo-175/automatic_backlight_dimming_on_the_xo_175.html Last accessed 03/02/13.
- **OLPC SKU** http://wiki.laptop.org/go/Manufacturing_data#XO-1.75. Last accessed 03/02/13.
- **OLPC XO** http://wiki.laptop.org/go/Especificacion_de_hardware Last accessed 03/02/13.
- **OLPC XO1** http://wiki.laptop.org/images/7/71/CL1A_Hdwe_Design_Spec.pdf) 
Last accessed 03/02/13.
- **OLPC XO1.5** http://wiki.laptop.org/images/f/f0/CL1B_Hdwe_Design_Spec.pdf Last accessed 03/02/13.
- **OLPC XO1.75** http://wiki.laptop.org/images/d/d4/CL2_Hdwe_Design_Spec.pdf 
Last accessed 03/02/13.
- **OLPC XO3** http://wiki.laptop.org/go/XO-3 Last accessed 03/02/13.
- **PSSC (1970)** Física. p. 679, Barcelona, España: Ed. Reverté.
Python (1990-2012)	http://www.python.org/ Last accessed 03/02/13.
- **PYTHON DOC** http://docs.python.org/library/ Last accessed 03/02/13.
- **PYTHON DOC MATH** http://docs.python.org/library/math.html Last accessed 03/02/13.
- **Roederer (1980)	Roederer,  J.** (1980).Mecánica Elemental. Buenos Aires, Argentina: Ed. Eudeba Manuales.
Site Google del Laboratorio de Física del Liceo Solymar Nº1 (2009)	http://sites.google.com/site/solymar1fisica/fisica-con-xo-investigacion-
Last accessed 03/02/13.
- **SUGARLABS MEASURE** http://wiki.sugarlabs.org/go/Activities/Measure Last accessed 03/02/13.
- **SUGARLABS SENSORS** http://wiki.sugarlabs.org/go/Activities/TurtleArt/Using_Turtle_Art_Sensors#Voltage_Mode: Last accessed 03/02/13.
- **SUGARLABS SUGAR** http://wiki.sugarlabs.org/go/What_is_Sugar%3F/lang-es
Last accessed 03/02/13.
- **SUGARLABS TURTLE BLOCKS** http://wiki.sugarlabs.org/go/Activities/Turtle_Art
Last accessed 03/02/13.
- **VERNIER LPL** http://www.vernier.com/downloads/logger-pro-linux/ Last accessed 03/02/13.  
- **VERNIER LQM** http://www.vernier.com/products/interfaces/lq-mini/ Last accessed 03/02/13.
- **Wikipedia Pulsioximetría** http://es.wikipedia.org/wiki/Pulsioximetr%C3%ADa y http://es.wikipedia.org/wiki/Ox%C3%ADmetro_de_pulso). Last accessed 03/02/13.
- **Wikipedia SUGAR** 	http://es.wikipedia.org/wiki/Sugar_(interfaz_gr%C3%A1fica_de_usuario)
Last accessed 03/02/13.

