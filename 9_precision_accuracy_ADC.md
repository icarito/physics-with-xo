# Accuracy and Precision of the Analog to Digital conversion (XO1, XO1.5, XO1.75)

## Accuracy:

Accuracy is the level of callibration of the measuring instrument to be analyzed. This value appears by comparing the results of measurements obtained with the same in respect to those obtained by using a second measuring instrument that is chosen as reference or standard.

In general it is recommended to check this periodically; for it an instrument is required that will serve as standard such as a high quality digital tester that has been callibrated as directed by the manufacturer. (For example, in our case, among others, we used a Fluke tester model 87 which must be callibrated "...once a year to make sure that it is working in accordance to its specifications." as explaind by its "Instructions Manual Fluke 87 TRUE RMS MULTIMETER", PN 834200, December 1988, Rev. 1. 3/93,  © 1993 John Fluke Mfg Co., Inc, Litho in U.S.A.)

## Precision:

In an ADC the the precision of conversion depends on its *resolution or number of bits (n)* and the *linearity* of the effected conversion. Other factors such as signal displacement **b** (offset) also affect precision. The original analog signal that we'll call **A** is converted into a given digital signal **D** by the following expression: D=int[(2^n/FS)*A+b] being FS (Full Scale) the maximum input voltage, and int[...] the integer part of the expression between square brackets.

For example, the AD conversor integrated to the sound board of the XO1 (Analog Devices 1888) has a 16bit resolution, and a maximum input voltage of 1.85 V (approx) therefore we are able to resolve the value in a series of 2^16=65536 steps of digitization.

In an ideal AD conversion, the function D= f(A) represents the direct proportionality. That is, the graph shows a straight line with the ordinal origin zero. In the real case, the measure of separation with respect to this ideal behaviour is measured by the *linearity* of the conversion. Measured deviations will limit the *precision* in the conversion done. Even with high resolution (n), if the AD conversion is strongly non-linear, precision will be low.

Source: Gil & Rodriguez (2001)

## Accuracy and precision of measures with XO1.

### Note

The results show ahead correspond to measures taken with an XO1, SKU5, model known as XO1 (CL1A) distributed by Plan Ceibal among students of public primary school when it first began. Beginning the month of June of 2012, an upgrade program was completed and students in 5th and 6th grade of Primary School got an XO1.75 in exchange for the old model.

### Accuracy and precision in measuring Voltage with XO1

Although the subject will be developed in detail in the following chapters, it may be intuitive to recognize that the following code written with the programming blocks of the TurtleBlocks (TB) Activity allows us to read the voltage from the external microphone input:

[insert ta screenshot here]

In order for the display of the value to become clear,, text may be combined at the "print" block by using the "addition" block, since it admits alphanumerical variables (text and numeric values); the program then could be as follows (volt monitor.ta):

Now that we know how to show measured values onscree, the questions that we'll attempt to answer is: What is the precision and accuracy of the XO measuring as a voltmeter? The answer involves a series of aspects to take into account:

#### Apreciation:

We may determine the appreciation of the XO as a voltmeter by using the programming shown above: the voltages are displayed onscreen to a centecimal of a Volt, therefore the **appreciation** is **0.01 V**.

#### Accuracy:

While it is true (as will be discussed further ahead) that there is no data dispersion in the order of a centecimal of a Volt, the values measured by the XO and the reference instruments independently or simultaneously usually don't coincide, therefore we must determine the accuracy of the obtained results, by calculating the callibration level of the XO1 as voltmeter; this can eb done by analyzing the graph Vref=f(Vxo1). The reference voltage Vref in this case was measured with the LQ mini interface.

[insert graph here]

Having plotted the values, two adjustments are included to the data set: for one part the linear adjustment **(y=mx+b)** and for the other the proportional **(y=ax)**; the first of them shows a **correlation coefficient ("Correlation")=1**, this implies that the data adjusts itself to the linear function optimally. In favor of simplicity, and observing thet ordinal at the origin of relative negligible value, we prefer to apply the proportional adjustment (instead of the referred linear) to relate the volt to each other.

While linear adjustment is satisfactory and prectically coincident with proportional adjustment, the proportionality coefficient **A** is not one, therefore measurements are not accurate. To recover accuracy we need to use this factor that we may call (in this case) *accuracy coefficient in voltage measurements*, and that we may abbreviate as **Cv**. In the case shown, the value is **0.9788**,  for this reason every volt measurement must be corrected with the following expression:

**Vcorrected = Cv.Voltage**

for this case, its:
**Vcorrected = (0.9788).Voltage**

"Voltage" being the value measured directly by the XO1.

Following are two ways to recover accuracy in volt measurements:
    1. one of them (cv product.ta) by using the "product" block (bottom, left) and the other
    2. (cv Python.ta) with the "Python block" that allows to include mathemathical formulas and commands in the Python language (the variable "box" was included in order to modify the variable value within the program "save in box 'cv' value 0.9788") (bottom, right)
