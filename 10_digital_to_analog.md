# Digital to Analog conversion

## Synthesis of sound on XO1

## Pippy Sugar Activity

    The XO1 can sythethize sounds by means of the digital to analog (DAC) converter integrated to its sound card. The programming of this synthesis can be done by programming Python code in the programming activity Pippy that comes included with SUGAR. The following code (Oscilador.py) may be used to program the synthesys of pure sounds of the desired frequency (in Hz), amplitude (arbitrary units), and duration (in seconds):

    [insert screenshot here]

## Turtle Blocks Sugar Activity (TB)

    It is also possible to achieve the synthesis with the TurtleBlocks Activity (v.109), with the python example "sinewave.py". The same may be loaded from the main menu:

    Main Toolbar/ Save/ Load Python Block/ "sinewave.py"/ Open

[insert screenshot]

When executing this example program, the speakers will emit a sound of 440 Hz of frequency (adjustable), fixed amplitude, and about 3 seconds of duration (non adjustable) corresponding to the note A (A4).

### Frequency range for synthetized sounds

The sound card of the XO1 synthetizes sounds between 30 Hz and 5000 Hz. The synthetized sounds correspond to practically pure sinusoidal (sine) signals, although the presence of other frequencies can be detected. En general, these components have much smaller amplitudes than the main signal, but they are measurable. The following graph shows some of them and the frequencies that accompany them; measurement was done on an XO1 emitting and an XO1.5 HS detecting the sound with the Measure Activity / Sound / Baseline Frequency:

[insert table here]

### Generated signal strength

According to technical specifications, the sound produced is emitted by the embedded speakers, which respond optimally to the range between 480 and 40kHz, fed by 1.4W each, for this reason, sounds generated between 30Hz and 480Hz will not sound well or may not be heard at all. To hear them it would be necessary to connect amplified speakers such as can be found in any desktop PC, to the earphone plug socket (green socket, located to the left of the screen, with maximal power of 30 mW and 32 ohm impedance).

In addition, this type of device will allow us to utilize the XO as a generator of mechanical oscillations of adjustable frequency, fundamental tool in a physics laboratory: especially if it is desired to study mechanical oscllations and waves.

It is possible to achieve quite acceptable results by using low cost amplifier and speakers. The maximum power of the amplifier, its build quality and that of the speakers, as well as their accepted frequency range, will allow for the production of desired frequencies. It is worth to keep in mind that especially when working with lower frequencies, they are generally outside the range of low cost PC amplified speakers and, however, are the ones that are needed to excite the oscillating mechanical systems such as mass-spring, sheets with a fixed side, wave bucket oscilators on water surfaces, etc.
