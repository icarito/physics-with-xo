# 7. Measure Activity (versions 31, 36 and 42)

The SUGAR graphical user interface includes a very potent tool for working in Experimental Physics and Musical Acoustics: The Measure Activity (Sugar Labs Measure); with it the XO is transformed into a single (XO1) or double (XO1.5 and XO1.75) stroke **oscilloscope** that enables us to analyze the sounds that the XO registers from its built-in microphone, or the voltage or resistance values that can be read through the external microphone input. Sound registered by the microphone may be analyzed as graphics that display the signal as a function of time (known as *oscilograms*), or as amplitude vs. frequency graphs (**A=f (f)**).

The Measure Activity can also read values of Voltage and Resistance through an audio cable connected to its external microphone socket. These values are displayed as detailed below in the description of the toolbar for version 31 (displays the voltage and resistance as an integer number to be calibrated), version 36 (displays measures of voltage and resistance already calibrated as Volt or Ohm values, and includes the ability to connect a second sensor) and version 42 (includes on-screen reference lines for fundamental frequencies and their harmonics for tuning diverse musical instruments).

## 7.1. Measure Activity version 31: Toolbar

In the area of the screen (divided in a grid by 22 horizontally and 14 vertically), an oscillogram is displayed Voltage=f(time) (Mode SOUND, baseline frequency), or an FFT Amplitude graph = f (frequency) (Mode SOUND, baseline frequency), or rather the value read by the Resistance or Voltage sensor (according to the selection). In the bottom bar, the integer resulting from the AD conversion is displayed, as shown in the example:

    Sensors, DC (connect sensor to pink 'Mic In' on left side of XO)
    Bias/Offset Disabled - Volts (-32768)

### Toolbar of the Measure Activity v.31

<style type="text/css">
    ol { list-style-type: lower-alpha; }
</style>

#### 1. Project Toolbar

![Project Toolbar](images/measure_31_a.png)

1. Project title
2. "Share" button (gray, not available)
3. Save a copy

#### 2. Configuration Toolbar, Sound, Time Base

![Configuration Toolbar / Time Base](images/measure_31_b.png)

1. "Time Base" (selected, see fourth icon in the top bar)
2. "Frequency Base" (grey)
3. "Freeze the display" button (pauses the image)
4. "Sampling interval" pull-down menu: each 30 sec, 2 min, 10 min, 30 min
5. "Capture sample now" button
6. "Create a trigger" pull down: rising edge, falling edge (enables a cursor to the center left of the screen)

**Sensitivity control**:

Sensitivity is adjustable by using the vertical slider located to the right of the screen (top = maximum sensibility).

**Horizontal sweep control**:

Slider bar (5th icon in the top bar)<br>
This control allows to select between 0.05 ms/DIV and 1.0 ms/DIV (by default: 0.5 ms/DIV). Settings are displayed in the bottom bar, as follows:

    Sound   Time Base
    X Axis Scale : 1 division = 0.5 ms

#### 3. Configuration Toolbar, Sound, Frequency Base

![Configuration Toolbar / Frequency Base](images/measure_31_c.png)

1. "Time Base" (gray)
2. "Frequency Base" (selected, see fourth icon in the top bar)
3. "Freeze the display" button (pauses the image)
4. "Sampling interval" pull-down menu: each 30 sec, 2 min, 10 min, 30 min
5. "Capture sample now" button
6. "Create a trigger" pull down: rising edge, falling edge

**Sensitivity control**:

Sensitivity is adjustable by using the vertical slider located to the right of the screen (top = maximum sensibility).

**Horizontal sweep control**:

Slider bar (5th icon in the top bar)<br>
This control allows to select between 10 Hz/DIV and 1000 Hz/DIV (by default: 500 Hz/DIV). Settings are displayed in the bottom bar, as follows:

    Sound   Time Base
    X Axis Scale : 1 division = 500 Hz

#### 4. Resistance sensor

![Resistance Sensor](images/measure_31_d.png)

1. Resistance sensor (selected, note the fourth icon in the top bar)
2. Voltage sensor (gray)
3. "Invert" button
4. Pull down: 1/10 s, 1 s, 30 s, 5 min., 30 min.
5. "Start logging" button

**Sensitivity control**:

Sensitivity is adjustable by using the vertical slider located to the right of the screen (top = maximum sensibility).

#### 5. Voltage sensor

![Voltage Sensor](images/measure_31_e.png)

1. Resistance sensor (gray)
2. Voltage sensor (selected, note the fourth icon in the top bar)
3. "Invert" button
4. Pull down: 1/10 s, 1 s, 30 s, 5 min., 30 min.
5. "Start logging" button

**Sensitivity control**:

Sensitivity is adjustable by using the vertical slider located to the right of the screen (top = maximum sensibility).

## 7.2 Measure Activity v36: Toolbar

When working with an XO1.5 or an XO1.75, this version of Measure will display the value of sensors connected to each channel, because the external microphone input for these models is stereo, allowing the measurement of two magnitudes simultaneously. When working with an XO1, only the left channel will be displayed.

The screen area (20 DIV abscissas x 14 DIV ordinates) may display:

1. A (double) oscillogram Voltage = f(time) (Sound mode, Time Base)
2. A (double) oscillogram FFT Amplitude = f(frequency) (Sound mode, Frequency Base)
3. A (double) oscillogram Measure = f(time) where ordinates are proportional to the value read for each Resistance or Voltage sensor (depending on selection)

In sensor mode, the bottom bar shows the value of Resistance or Voltage as read by each of the sensors connected to the left channel (CHL) and right channel (CHR) of the XO1.5 or 1.75, as the example shows:

    Resistive sensor (connect sensor to pink 'Mic In' on left side of XO)
    Resistance (Ohms)   (420000000) (12673050)

### Toolbar of the Measure Activity v.31

#### 1. Project Toolbar

![Project Toolbar](images/measure_36_a.png)

