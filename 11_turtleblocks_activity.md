# Turtle Blocks Activity (TB)

The Sugar Graphical User Interface includes several Activities that can be used to learn how to program, known as programming environments. Some of them are Pippy, Etoys, Scratch and Turtle Blocks. The latter, Turtle Blocks Activity (Sugar Labs), is the one we'll use throughout this work. It is a development environment inspired in the LOGO programming language, created -among others- by the southafrican mathematician Seymour Papert in the decade of 1960; frequently identified with a turtle that drew on screen guided by programming that a user wrote, generally children and teenagers, as it was widely used to teach first steps in programming.

Initially called Turtle Art, (or Turtleart) this activity includes, among others, the ability to read voltages and resistances connected to the external microphone socket of the XO.

## Toolbars of TB version 109

1. Activity toolbar (Project toolbar):
    
    [insert screenshot here]
    
    1. Project Title
    2. Share button
    3. Save copy

2. Edit Toolbar:
    
    [insert screenshot here]

    1. Copy
    2. Paste

3. Save Toolbar:

    [insert screenshot here]

    1. Instant save
    2. Save as HTML
    3. Save as LOGO
    4. Save as Image
    5. Import from Journal
    6. Load Python block
    7. Load examples

4. View Toolbar:

    [insert screenshot here]

    1. Fullscreen
    2. Cartesian coordinates
    3. Polar coordinates
    4. Centimeter coordinates
    5. Rescale coordinates
    6. Grow blocks
    7. Shrink blocks

5. Palette Toolbar:

    [insert screenshot here]

    1. Turtle commands palette
    2. Pen commands palette
    3. Pen colors palette
    4. Numerical operators palette
    5. Flow operators palette
    6. Variable blocks palette
    7. Sensor palette
    8. Media object palette
    9. Aditional options palette
    10. Presentation templates palette
    11. Trash bin
    12. Hide blocks

6. Help toolbar

    [insert screenshot here]

    Enables contextual help

7. [insert icon here] CLEAN: Clean drawing in the canvas
8. [insert icon here] RUN: Runs the program (*Start* block) (maximum speed)
9. [insert icon here] RUN SLOWLY: Runs the program at low speed
10. [insert icon here] DEBUG: Runs the program block by block (to review the programming)
11. [insert icon here] STOP TURTLE: Stops the execution of the program (red: RUN / black: STOP)
12. [insert icon here] STOP: Closes Turtle Blocks Activity

[insert icon here] HIDE BLOCKS: in this state, it shows blocks; when fill color is yellow, it hides them. You may toggle between views by clicking this icon found on the right of the "trash bin".

## Palettes

1. Turtle commands palette
    [insert screenshot here]
2. Pen commands palette
    [insert screenshot here]
3. Pen colors palette
    [insert screenshot here]
4. Numerical operators palette
    [insert screenshot here]
5. Flow operators palette
    [insert screenshot here]
6. Variable blocks palette
    [insert screenshot here]
7. Sensor palette
    [insert screenshot here]
8. Media object palette
    [insert screenshot here]
9. Aditional options palette
    [insert screenshot here]
10. Presentation templates palette
    [insert screenshot here]
11. Trash bin
    [insert screenshot here]

## Help for each block in palettes (TB v.109)

We've included the help texts as they appear when invoked from inside the Activity: they consist of a brief description of the action that each block executes. An additional column with additional information has been included.

### Turtle commands palette

| Block     | Help (original)       | Additional clarification |
|-----------|-----------------------|--------------------------|
| forward   | Moves turtle forward  | It has a numerical block attached where you must indicate how much to move forward (by default: 100) |
| back      | Moves turtle backward | It has a numerical block attached where you must indicate how much to move backward (by default: 100) |
| clean     | Clears the screen and reset the turtle | Erases the canvas, places the turtle at location (0,0), lowers the pen, selects red color, heading=0. It may be executed by clicking the eraser button (7th icon from main toolbar) |
| left      | Turns turtle counterclockwise (angle in degrees) | It has a numerical block attached where you must indicate how much to turn (by default: 90°) |
| right     | Turns turtle clockwise (angle in degrees) | It has a numerical block attached where you must indicate how much to turn (by default: 90°) |
| arc       | Moves turtle along an arc | It has a numerical block attached where you must indicate how much to turn (by default: 90°) as well as the desired radius (by default: 100) |
| setxy     | Moves turtle to position xcor, ycor; (0, 0) is in the center of the screen. | It has a numerical block attached where you must indicate the x coordinate (by default: 0) as well as the y coordinate (by default: 0) of the point on the screen you wish the turtle to be. |
| seth      | Sets the heading of the turtle (0 is towards the top of the screen.) | It has a numerical block attached where you must indicate the angle the turtle body will be looking at for moving forward (by default: 0) |
| xcor      | Holds current x-coordinate value of the turtle (can be used in place of a number block) | - |
| ycor      | Holds current y-coordinate value of the turtle (can be used in place of a number block) | - |
| heading   | Holds current heading value of the turtle (can be used in place of a number block) | - |

### Pen commands palette

| Blocks    | Help (original) | Additional clarification |
|-----------|-----------------|--------------------------|
| penup     | Turtle will not draw when moved. | - |
| pendown   | Turtle will draw when moved. | - |
| setpensize | Sets size of the line drawn by the turtle. | It has a numerical block attached where you must indicate the numeric value for the line width (by default: 5) |

