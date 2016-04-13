# Accuracy and Precision of the Analog to Digital conversion (XO1, XO1.5, XO1.75)

## Accuracy:

Accuracy is the level of calibration of the measuring instrument to be analyzed. This value appears by comparing the results of measurements obtained with the same in respect to those obtained by using a second measuring instrument that is chosen as reference or standard.

In general it is recommended to check this periodically; for this an instrument is required that will serve as standard such as a high quality digital tester that has been calibrated as directed by the manufacturer. (For example, in our case, among others, we used a Fluke tester model 87 which must be calibrated "...once a year to make sure that it is working in accordance to its specifications." as explained by its "Instructions Manual Fluke 87 TRUE RMS MULTIMETER", PN 834200, December 1988, Rev. 1. 3/93,  © 1993 John Fluke Mfg Co., Inc, Litho in U.S.A.)

## Precision:

In an ADC the precision of conversion depends on its *resolution or number of bits (n)* and the *linearity* of the effected conversion. Other factors such as signal displacement **b** (offset) also affect precision. The original analog signal that we'll call **A** is converted into a given digital signal **D** by the following expression: D=int[(2^n/FS)*A+b] being FS (Full Scale) the maximum input voltage, and int[...] the integer part of the expression between square brackets.

For example, the AD conversor integrated to the sound board of the XO1 (Analog Devices 1888) has a 16bit resolution, and a maximum input voltage of 1.85 V (approx) therefore we are able to resolve the value in a series of 2^16=65536 steps of digitization.

In an ideal AD conversion, the function D= f(A) represents the direct proportionality. That is, the graph shows a straight line with the ordinal origin zero. In the real case, the measure of separation with respect to this ideal behaviour is measured by the *linearity* of the conversion. Measured deviations will limit the *precision* in the conversion done. Even with high resolution (n), if the AD conversion is strongly non-linear, precision will be low.

Source: Gil & Rodriguez (2001)

## Accuracy and precision of measures with XO1.

### Note

The results show ahead correspond to measures taken with an XO1, SKU5, model known as XO1 (CL1A) distributed by Plan Ceibal among students of public primary school when it first began. Beginning the month of June of 2012, an upgrade program was completed and students in 5th and 6th grade of Primary School got an XO1.75 in exchange for the old model.

### Accuracy and precision in measuring Voltage with XO1

Although the subject will be developed in detail in the following chapters, it may be intuitive to recognize that the following code written with the programming blocks of the TurtleBlocks (TB) Activity allows us to read the voltage from the external microphone input:

[insert ta screenshot here]

In order for the display of the value to become clear, text may be combined at the "print" block by using the "addition" block, since it admits alphanumerical variables (text and numeric values); the program then could be as follows (volt monitor.ta):

Now that we know how to show measured values onscreen, the questions that we'll attempt to answer is: What is the precision and accuracy of the XO measuring as a voltmeter? The answer involves a series of aspects to take into account:

#### Appreciation:

We may determine the appreciation of the XO as a voltmeter by using the programming shown above: the voltages are displayed onscreen to a centecimal of a Volt, therefore the **appreciation** is **0.01 V**.

#### Accuracy:

While it is true (as will be discussed further ahead) that there is no data dispersion in the order of a centecimal of a Volt, the values measured by the XO and the reference instruments independently or simultaneously usually don't coincide, therefore we must determine the accuracy of the obtained results, by calculating the calibration level of the XO1 as voltmeter; this can be done by analyzing the graph Vref=f(Vxo1). The reference voltage Vref in this case was measured with the LQ mini interface.

[insert graph here]

Having plotted the values, two adjustments are included to the data set: for one part the linear adjustment **(y=mx+b)** and for the other the proportional **(y=ax)**; the first of them shows a **correlation coefficient ("Correlation")=1**, this implies that the data adjusts itself to the linear function optimally. In favor of simplicity, and observing an ordinal at the origin of relative negligible value, we prefer to apply the proportional adjustment (instead of the referred linear) to relate the volt to each other.

While linear adjustment is satisfactory and practically coincident with proportional adjustment, the proportionality coefficient **A** is not one, therefore measurements are not accurate. To recover accuracy we need to use this factor that we may call (in this case) *accuracy coefficient in voltage measurements*, and that we may abbreviate as **Cv**. In the case shown, the value is **0.9788**,  for this reason every volt measurement must be corrected with the following expression:

**Vcorrected = Cv.Voltage**

for this case, its:
**Vcorrected = (0.9788).Voltage**

"Voltage" being the value measured directly by the XO1.

Following are two ways to recover accuracy in volt measurements:
    1. one of them (cv product.ta) by using the "product" block (bottom, left) and the other
    2. (cv Python.ta) with the "Python block" that allows to include mathematical formulas and commands in the Python language (the variable "box" was included in order to modify the variable value within the program "save in box 'cv' value 0.9788") (bottom, right)

[insert turtle code here]

This coefficient depends on each particular XO we are working with, so we must determine it for each of them. To know the dispersion level for *accuracy coefficients in voltage measurements*, 9 different XO1 laptops were used to measure the same voltage, which was later compared with the reference instrument (Vref=1.529 V).

We graph **Cv** for each XO1 as a function of N, an ordinal arbitrary number that identifies each of the netbooks used:

[insert dispersion graph here]

It can be deduced that according to our measurements, the values obtained for **Cv** do not differ more than 4% (XO1 ordinal N=6) with respect to the reference so it is worth to introduce this correction only in applications that require it (where accuracy in voltage reading is fundamental).

#### Precision:

##### Precision associated with statistical dispersion of measurements:

Now we must determine what level of statistical dispersion exists when measuring the same voltage repeatedly. We calculate the average of the series V_average, the standard deviation for the measure **σ-s** and from it the standard deviation for the average, **σ-est** (the parameter that allows to determine the dispersion of measurements with respect to their average value), and N-op, the optimal number of measurements to make.

Summary[insert footnote]:

(we summarize the expressions that were used when doing calculations)

*Given a series of N values xi (resulting from performing measurements of the same physical magnitude under identical conditions), we calculate the arithmetical average xavg with:*

[insert formula here]

*We define the deviation εi of each measurement xi with respect to an average as*

εi = xi - Xavg

*Supposing that the series of measurements shows a normal distribution, it makes sense to calculate the standard deviation for each measurement:*

[insert formula here]

*For N->infinite and the above conditions, 68% of values will be found within the interval: X+/-σs*

*Nevertheless the uncertainty associated with dispersion is determined starting from a previous value, calculating standard deviation from the average with the expression:*

[insert formula here]

*Once nominal uncertainty σnom is determined in association with a measurement (which can be considered, in a simplified form and under certain conditions, to be equal to the appreciation of the utilized measuring instrument), we will be able to calculate the optimal number Nop of measurements to make. The criteria used here is to make enough measurement until the condition σest~=σnom allows to obtain the following expression:*

[insert formula here]

The combined uncertainty can be obtained with:

[insert formula here]

To reach our goal, we will compare the measurements from measuring a given voltage with the reference tester Fluke 87, the AD LQ mini (Vernier), and the XO. For this the TurtleBlocks Activity will be used to program the reading of 50 consecutive voltage readings, averaging them and showing the result on screen.

Programming is as follows: 

[insert turtleblocks program here]

This program (Vpromedio.ta) is executed 30 times for the same voltage, then calculates the standard deviation σs for the set of measurement if there are differences from each other.

The values resulting from the procedure show that there is no dispersion in the order of a centesimal of a volt, so that value will be taken as the uncertainty associated to the precision for statistical dispersion and appreciation combined.

##### Precision associated with linearity

##### Calculation of the dispersion level in measurements of Voltage with respect to proportional adjustment (once the XO1 has been calibrated)

Once the calibration level has been recovered by means of the introduction of the Cv coefficient, we must calculate how far apart the (corrected) voltages measured by the XO1 are from the proportional adjustment. For this we have calculated the relative percent deviations of voltages with respect to the proportional adjustment. The results are summarized in the following graph, where the relative percentual εr% is observed as a function of the reference voltage Vref (in this case it was measured with the LQ mini interface):


[insert graph here]

It can be concluded that hte set of values maintains a low percentual dispersion with respect to the applied adjustment, that don't exceed 1.5%.

### Conclusions

a- When used as a Voltmeter directly, measurements can be made that may differ in accuracy up to 4% with respect to a reference instrument.

In order to obtain more accurate results, before you begin measurements, and for each XO in particular, the accuracy coefficient Cv will need to be calculated. This factor must multiply the "voltage" sensor block each time that it is used.

b- The uncertainty of the XO1 as voltmeter is:

    -/+(0.01V +1.5% of the value displayed onscreen)

#### Input impedance of the XO1 as voltmeter

An ideal measuring device would be capable of obtaining a measurement for the system being studied without taking energy from it, that is, without intercting. Such a measuring device does not exist. Real measuring devices are constructed in such a was as to obtain a measurement from the minimum interaction with the system being measured.

In the particular case of voltmeters, this condition would be met if their input impedance was infinite. The reference tester that we used has (according to the manufacturer) an input impedance of 10MΩ. The data relative to the XO1 indicate that its input impedance is in the order of 150 kΩ.
