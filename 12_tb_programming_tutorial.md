# 12 Brief tutorial of introduction to programming using the TurtleBlocks Activity (TB).

## Introduction: 

The "Physics with XO" project aims at popularizing the knowledge necessary to turn the XO into an instrument for acquisition and processing of physical measurements of elementary level. This task involves a body of knowledge including the design, installation and calibration of sensors and the programming that will process the information acquired. 

The first task is simple and can be done without deep knowledge of electricity or electronics. However, the task of programming is much more complex, given that the project is based on the possibility to design a large number and variety of applications based on a reduced set of sensors. While all programs written by the author are included for use, the most important lesson from this work is the possibility to modify, rewrite or (as superior objective) to create some completely new programs adapted to the objectives of the reader.

This is why this brief tutorial to programming is included.
 
### Note:

1. Before starting it should be made clear that the author is not a programmer nor does he have the specific teaching skills necessary to convey this knowledge. This tutorial is only justified by the desire to convey the project in the hope that very competent people could assist readers to overcome any error committed here.

2. Included content can be supplemented with the TB programming tutorial on the wiki of SUGAR LABS (SUGARLABS TURTLE BLOCKS) (in English). Those wishing to delve deeper in the subject, should consult the tutorial "BUTIÁ TORTUGA" (in Spanish), dramatically expanded with their educational robotics applications by the MINA group, creators of BUTIÁ Robot. [insert footnote here]

PYTHON DOC documentation should also be consulted.

3. All programming can be downloaded from:
https://sites.google.com/site/solymar1fisica/programas-tb

## 12.1 Frecuently used features of the TB Activity:

This activity allows us to draw on the screen by executing orders that are given to the turtle and get translated into movements; in this way, we can draw line segment and arcs, and any figure that can be imagined as a combination of both. The stroke width, length, color, tone, etc. can be selected. Polygons can be drawn and then colored.

We will use these capabilities to draw Cartesian axes and draw charts on the screen by joining the points successively occupied by the turtle. In cases where this sequence is very dense, the stroke will look as corresponding to a continuous function.

It can also display text on-screen, the value of the magnitude measured by a sensor at a given moment (or combination of both), a photo taken by the built-in digital camera (with block *show* of the *Media object palette*) or also data being measured may be permanently showed on-screen by displaying the status bar (this is achieved with block *print* from the *Additional options palette*).
 
A very interesting feature of this Activity, is the ability to synthesize human voice to output a text message, a numeric value or a combination of both; this is achieved by running a Python programming block called *speak.py* (TB v.109) or by running the *speak* block (TB v.130) from the *Media object palette*. As previously described, TB allows to synthesize a sinusoidal signal of adjustable frecuency (and produce an audible sound for example), this time either by executing the Python programming block called *sinewave.py* (TB v.109) or by executing the *sinewave* block (TB v.130) from the *Media blocks palette* (in this case the duration of the output signal may also be selected).

**Note: the following examples relate to TB v.109 running on XO1 except those that refer to the 130 version which is indicated explicitly in brackets (with name * .ta).**

## CONSTRUCTION OF GEOMETRIC FIGURES.

### Example 1 to draw a square:

The canvas on which the turtle moves can be interpreted as a cartesian space with the origin (0, 0) located at the center (initial position of the turtle at the beginning of any TB program's execution) and border positions -600 to +600 (horizontal axis **x**) and -450 to +450 (vertical axis **y**). 

We'll start by drawing a square of side "100" (Number of turtle steps):

Case A: One way to do it is to command the turtle to occupy the vertices of the square in order (from left-bottom tracing clockwise), as shown in the following program (*cuadrado por vértices.ta*): 

[insert blocks]

To run it, you must either press the icon (run) [icon run here], or click in the topmost block "start" (which executes the main routine of the program). The block *clean* clears the canvas before starting any action.

If you want to know what action each block performs, the program can be executed by pressing the icon (debug) [icon debug here] which runs the program block by block, modifying the color of the block that is running at every moment; this mode allows understanding what it is doing and detect possible errors in programming.

**Case B:** An alternative is to have the turtle move forward and turn 90 degrees (an angle that we will call *external*, supplemental to internal) four times, as shown in the following example (*cuadrado adelante derecha.ta*):

[insert blocks]

Here you can see that the forward and right blocks repeat themselves, so we could run the same action without retyping, adding a repeat block as shown in the following example (cuadrado repetir 4 .ta): 

{insert blocks}

Case C: 

{insert blocks}

In this case we have included the blocks hidden blocks (not to be displayed while the program is running), full screen (showing only the canvas and the turtle strokes hiding toolbars and palettes) and set color/random (0, 100) (randomly changing the stroke color on each new side of the square). 

This examples show that it is possible to perform the same action in different ways, each written in a more sumarized way than its predecessor. The idea is not to repeat blocks, by including blocks as repeat, while, forever, until, etc.

Example 2 draw an equilateral triangle:

We will make this track (tri?ngulo repetir 3.ta) recalling that internal angles thereof are 60 degrees. But as our turtle makes use of external angles, we will use the corresponding 120 degrees. We will proceed in a similar way to the programming of previous case C:

{insert blocks}

Example 3 draw a regular polygon of N sides. Introduction to using variables ("box") in TB: 

Comparing the last two programs we see that the set of blocks within the repeat block runs a number of times that matches the "Number of sides" of the polygon to draw, and that the external angle that is written along the right block (responsible for spinning the turtle) corresponds to the value (360 / number of sides). This allows us to introduce the concept of variable, an amount that can be entered as a parameter and can then be displayed on screen, used for later calculations, etc.: In TB variables are stored in "boxes": box 1, box 2, or in a box whose name we choose. In this case we create two boxes: 1."Number of sides" and 2."external angle". The value corresponding to the box "Number of sides" should be written in it before running the program, while the value of the box "external angle" is calculated from that. The following program (pol?gono cajas .ta) draws a triangle, a square, a pentagon, etc. according to the value initially enter in the box "Number of sides" (values 3, 4, 5, etc.). Cases corresponding to the values 3 and 5 are shown which produce the layout of an equilateral triangle and a pentagon:

{insert blocks}

{insert blocks}

Display on-screen text, numerical values and images. Introduction to data types, operators and control structures in TB:

To do this simply use the block show connected to:
1. A block [insert block icon] (string of characters) you want to display
2. A block [insert block icon] (real or integer numeric value) or
3. The contents of a variable "box". This block may be the result of reading a sensor connected to the external microphone input of the XO.


It can be used to display text and numeric value at the same time using the addition operator and to clarify the interpretation of the displayed value. The following example (mostrar volumen.ta) displays on screen the numeric value corresponding to the volume of sound recording the microphone of the XO:

{insert blocks}

If we want to continually monitor the volume, we should write a program (monitor de volumen.ta) that permanently repeats the above action. For this we will use the block forever, but attached to the print block which will show it in a status bar that is displayed on the bottom of the screen. We will do this because show writes from the initial position of the turtle and, if we don't want to do it over what is already written, we must reposition before repeating the action (will be used to generate tables of values below). Monitor volume shown below:

{insert blocks}

To complete the presentation of data types in TB and displays on screen, we should add a logic condition: if the volumen is greater than a certain value, the camera will take a photo and it will be shown on screen.  

For this we use the if-then block (from the flow operators palette) next to the greater than operator: in this way, if the condition (type of logical or boolean data that can only take two values truth of false) is truth, the program (si volumen 100 saca foto.ta) runs the lines that follow the then: 
  
{insert blocks}

The stop action block connected at the lowest location in the set stops execution of the block forever once the condition is met and the picture is displayed. If you want to continue program execution indefinitely that block should be removed. This permanent execution without stopping condition is called a loop.
 
The following example (storyboard 36.ta) is a program that triggers the camera 36 times in succession, placing a photo next to each other forming a 6x6 matrix to cover the entire screen. This is an example that can be used as entertainment for the younger children.

{insert blocks}

A slight modification (storyboard.ta) repeats the action indefinitely until the program execution is interrupted:

{insert blocks}

With the show block, any other type of media objects, in particular videos can also be displayed on screen: these objects must be stored in the Journal of XO.




Emission of sounds and speech synthesis. Introduction to the Python block

TB's ability to make sounds of adjustable frequency was discussed in Chapter 10, the digital to analog conversion (by loading the Python [icon here] programming sample block called sinewave.py).

Another interesting TB capacity refers to the possibility of issuing a spoken message using the Python programming block speak.py included as a sample in the folder pysamples. This code can be included in our TB program by loading the block Python; this procedure is described in Chapter 11 Activity TURTLE BLOCKS (TB).

The following example (si volumen 100 habla .ta) is a modification of the previous si volumen 100 saca foto .ta which makes the XO "talk" when the volume recorded by the microphone exceeds the value (arbitrary) 100. In this case the message "the sound volume is very high" plays:

{insert blocks}

Note: You must remember that every time this program is copied to another XO, the Python block is "empty", so the process "load" and save in the Journal should be repeated. From then it runs correctly each time it is invoked. Comment programming block is added as a reminder of this fact you can forget.

If working with TB version 130 and later, this problem of "emptying" does not exist because the block is used to talk like (si volumen 100 habla v130.ta) is shown below:

{insert blocks}

Generalization: as in the two examples above (speak.py and sinewave.py), within a programming TB can enter a portion of code written in Python of several lines by introducing the block Python. This can facilitate common tasks that appear as samples in the pysamples folder and can not be programmed using the TB blocks available. You can also write an absolutely original block in Activity Pippy (for example), save it in the Journal with myblock name, and then load it into our program.


Access to time measurements and calculations of mathematical functions. Introduction to the Python function block

[icon here] A block having a great versatility when programming is Python function block, unlike the block Python, allows the execution of a command line or single programming; for example, if you want to make time measurements we can invoke from this block the Python time () command, and obtain the current time, measured with respect to an arbitrary origin (known as epoch). If we set a timer to the thousandth of a second, we can write the following program (Cron?metro (ms) .ta):

{insert blocks}

The program begins saving the initial instant in a box we will call "ti" to then permanently print on sreen the result of subtracting to the current time (previously stored in the box "tf") the value of "ti". As time () it is expressed in seconds, multiply the result by 1000 so that on screen appears the interval in milliseconds. Of the operation "1000x(tf-ti)" we take only the integer part, by running the Python command int ().

We see another example of programming (reloj.ta) using commands localtime().tm_hour and localtime().tm_min within Python function blocks to program the on-screen display of the current time:

{insert blocks}

In addition to the above, this block allows us to perform advanced mathematical calculations of one (x), two (x, y) or three (x, y, z) variables. To select the number of parameters or variables, you must press the "+" sign, located in the lower left corner of the block. By default the block's output is: f (x) = x with x = 100. To perform any other calculations, the funtion must be written within the block function "f(x)" with the proper syntax that can be consulted in PYTHON DOC MATH. The following example (B?skara.ta) is the programming that obtains the roots of a quadratic equation after the imput of the a, b and c coefficients (storing them in "boxes" of the same name):

{insert blocks}

In this case it is x? - x - 10 = 0, displaying on screen:

{insert blocks}

The previous program could be constructed by joining blocks of the numeric operators palette, but it would be longer and less intuitive.

Using actions and storing values in the stack: empty stack, push and pull blocks.

It may be noted that the example program immediately preceding (B?skara.ta) is written based on two columns of blocks: the main column headed by [insert icon] and a secondary column headed by [insert icon]. When being invoked with [insert icon] the latter is run from the main body of the program.  

This way of writing complex programs based on specific modules that perform simple tasks is recommended to gain in simplicity, clarity and reuse actions that are repeated in various programs. In TB these subroutines or sub-programs are called actions and to work with them the action1, action2, or named action blocks are used, the latter very useful for making more readable and intuitive the drafting of the program.

After having introduced the concept of variable in TB with the use of "boxes", we present an alternative that expands this type of storage possibilities: the stack. This consists of a series of memory addresses that can get load of values by the push block for subsequently use, in this case by the pull block. The values ??are stored as when proceeding to fill a box with packages: the first to enter will be the last to leave (so called FILO first in last out).

It is clear that any program that makes use of the stack should begin erasing its contents by the empty stack block. If during the step of test-programming you want to know the content, the show stack block can be used.

We will show here an application program, which monitors the current time and when it matches any of the values ??stored in the "stack" (through the action cargar timbres (load alarms)), issues a sound of 1000 Hz frequency.



For getting current time, the commands localtime().tm_hour (hour) and localtime().tm_min (minutes) are used. The action cargar timbres (load alarms) empties the stack and stores the time values that match with an input or output timbre (alarm).  The action puesta a punto (set up) stores in the box timbre (alarm) the time nearest to the current time. When both values match, there is an output sound 
correspondant the alarm.

This example (timbres solymar1.ta) can be used to automatically ringing doorbells in and out of classes at a high school. The current time and the time to the next ring are displayed:

NOTE: The set of blocks within the action cargar timbres may collapse in a single block by clicking the "-" sign.

{insert blocks}


Programming deployment of value boxes onscreen

A very common programming of any Data acquisition software is the generation and on-screen display  frame of values. At
following example table of values shown in column shown
left values x and in the right column the result of the function x
given, in this example, by the expression f (x) = x 2 +5.

To do this, we must use the block show repeatedly (iteration):
for each iteration the variable x is incremented by one unit and calculated the
value taken by the function f (x) chosen.
