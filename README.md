# Python Speedcubing Timer

Made a timer for speedcubers similar to csTimer after ~ 2 weeks of learning Python.


## Overview

The idea is to create an interface with Python that generates a randomized legal scramble, allows the solver to time their solve for said scramble and write down all their times.


## Features

- Randomized legal scramble in cube notation (such as R, U, F, ...)
- Generating a "clean" scramble (no repeating moves, etc.)
- Hold-space-to-start timer
- A table where all previous times are collected
- Graphic visualisation for how the cube should look for said scramble


## How it works

### Scramble generation

The program constantly generates a random move and checks its validity. For example, the program is constantly checking that no two consecutive moves are moving the same face.

### Timer

Checks if the solver has been holding space for long enough. If so, the timer will turn green and releasing space will make time start counting down.
The time is constantly updating in real time. Pressing space will stop the timer. The time is then collected to a table and a new scramble gets generated.

### Graphic scramble display

The program keeps track of each sticker on the cube and checks how each move of the scramble moves the pieces around. As a result, the program shows how the cube looks from each side once scrambled.


## Challenges

### Generating a valid and clean scramble

There are multiple special cases that have to be taken into account to avoid unwanted combinations. The program has to keep track of previous moves and compare them to the newly generated one.

### Accurately mapping out the colors of the scrambled cube

The program is forced to track how each sticker on each piece moves for every possible move with complete accuracy. The implementation was by far the most tedious part of the project.

### GUI Development

Figuring out all the logic needed to make the timer, scramble, cube graphics and solve history all work the way the should across multiple iterations was somewhat challenging, since this was my first time using Tkinter.


## What I learned

- Programming with Tkinter and making GUI
- Event-driven programming
- Simply getting comfortable with the fundamentals of Python and how to use them together in one big picture


## Future improvements

- Statistics (Best single, Ao5, Ao12, Best average, ...)
- Ability to look at a previous time and the corresponding scramble
- Scrambles for other puzzles (2x2, 4x4, ...)
- Better-looking interface
- Timer during inspection (max 15s of inspections in WCA competitions)


## Images & Videos

Interface with scramble and its graphic visualisation
<img width="1919" height="1032" alt="kuva" src="https://github.com/user-attachments/assets/911aeffc-a07d-4dbf-96a9-96ce282313f2" />


Example solve
https://drive.google.com/file/d/1y7zknjSzN-ZEnbs_nNQRqEwnNNSJgYQP/view?usp=sharing
