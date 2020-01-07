# Micromouse

This project is a simulation of a micromouse robot. The goal is to find the exit of a maze. The robot is autonom and go through the maze by itself.

![Maze](https://github.com/TanguyCavagna/Micromouse/img/maze.png)

<hr>

# Installation

### Clone
 - Clone this repo to your local machine using ```https://github.com/TanguyCavagna/Micromouse.git```

### Setup

> you need to install this package

```
$ pip intall pygame
```

To run it, simply execute the ```app.py``` file and ENJOY !

# To go deeper

If you want to chage the maze, simply go to https://github.com/micromouseonline/micromouse_maze_tool/tree/master/mazefiles/cfiles.
Choose a file, open it and copy the hexadecimal values.
```
 0x0E, 0x0A, 0x0A, 0x08, 0x0A, 0x0A, 0x0A, 0x08, 0x0A, 0x0A, 0x08, 0x0A, 0x0A, 0x08, 0x0A, 0x09,
 0x0C, 0x0A, 0x08, 0x02, 0x0A, 0x0A, 0x0A, 0x00, 0x0A, 0x0A, 0x02, 0x0A, 0x09, 0x06, 0x08, 0x01,
 0x04, 0x09, 0x05, 0x0C, 0x0A, 0x0A, 0x0A, 0x02, 0x08, 0x0A, 0x0A, 0x0A, 0x00, 0x0B, 0x05, 0x05,
 0x05, 0x05, 0x05, 0x04, 0x0A, 0x0A, 0x0A, 0x09, 0x05, 0x0C, 0x0A, 0x0A, 0x03, 0x0C, 0x03, 0x05,
 0x05, 0x05, 0x05, 0x06, 0x0A, 0x0A, 0x09, 0x05, 0x04, 0x03, 0x0E, 0x08, 0x0A, 0x02, 0x0B, 0x07,
 0x05, 0x05, 0x06, 0x0A, 0x08, 0x0A, 0x02, 0x02, 0x03, 0x0E, 0x09, 0x06, 0x0A, 0x0A, 0x0A, 0x09,
 0x05, 0x06, 0x0A, 0x08, 0x02, 0x0A, 0x08, 0x0A, 0x0B, 0x0C, 0x01, 0x0C, 0x08, 0x08, 0x09, 0x05,
 0x04, 0x0A, 0x09, 0x06, 0x0A, 0x09, 0x05, 0x0C, 0x09, 0x05, 0x05, 0x05, 0x05, 0x05, 0x05, 0x05,
 0x05, 0x0D, 0x04, 0x08, 0x09, 0x05, 0x05, 0x06, 0x02, 0x03, 0x04, 0x00, 0x02, 0x03, 0x05, 0x05,
 0x05, 0x05, 0x05, 0x05, 0x05, 0x05, 0x06, 0x0A, 0x09, 0x0E, 0x01, 0x06, 0x0A, 0x0A, 0x03, 0x05,
 0x05, 0x05, 0x04, 0x02, 0x02, 0x02, 0x08, 0x08, 0x01, 0x0F, 0x06, 0x0A, 0x09, 0x0E, 0x0A, 0x01,
 0x04, 0x01, 0x05, 0x0C, 0x0A, 0x0A, 0x03, 0x05, 0x04, 0x09, 0x0E, 0x0A, 0x02, 0x08, 0x09, 0x05,
 0x05, 0x05, 0x05, 0x04, 0x0A, 0x0A, 0x0A, 0x03, 0x07, 0x06, 0x0A, 0x0A, 0x09, 0x07, 0x05, 0x05,
 0x07, 0x05, 0x05, 0x06, 0x0A, 0x0A, 0x0A, 0x08, 0x08, 0x0A, 0x0A, 0x0A, 0x00, 0x0B, 0x05, 0x05,
 0x0C, 0x03, 0x06, 0x0A, 0x0A, 0x08, 0x0A, 0x03, 0x06, 0x0A, 0x0A, 0x0A, 0x01, 0x0C, 0x02, 0x01,
 0x06, 0x0A, 0x0A, 0x0A, 0x0A, 0x02, 0x0A, 0x0A, 0x0A, 0x0A, 0x0A, 0x0A, 0x02, 0x02, 0x0A, 0x03,
```

To replace the current maze in the project, open the ```models/Maze.py``` file and change the ```world_maze```vairable.
```python
world_maz = np.array([
    0x0E, 0x0A, 0x0A, 0x0A, 0x08, 0x0A, 0x0A, 0x0A, 0x0A, 0x0A, 0x0A, 0x0A, 0x08, 0x0A, 0x0A, 0x0B,
    0x0E, 0x08, 0x08, 0x0A, 0x02, 0x0A, 0x0A, 0x08, 0x08, 0x0A, 0x0A, 0x0A, 0x02, 0x08, 0x08, 0x0B,
    0x0C, 0x03, 0x06, 0x0A, 0x0B, 0x0C, 0x0A, 0x01, 0x04, 0x0A, 0x09, 0x0E, 0x0A, 0x03, 0x06, 0x09,
    0x06, 0x09, 0x0C, 0x08, 0x08, 0x00, 0x0A, 0x00, 0x00, 0x0A, 0x00, 0x08, 0x08, 0x09, 0x0C, 0x03,
    0x0C, 0x03, 0x05, 0x05, 0x05, 0x06, 0x0A, 0x01, 0x04, 0x0A, 0x03, 0x05, 0x05, 0x05, 0x06, 0x09,
    0x06, 0x09, 0x05, 0x05, 0x06, 0x0A, 0x0B, 0x06, 0x03, 0x0E, 0x0A, 0x03, 0x05, 0x05, 0x0C, 0x03,
    0x0C, 0x02, 0x02, 0x02, 0x0A, 0x0A, 0x0A, 0x0A, 0x0A, 0x0A, 0x0A, 0x0A, 0x02, 0x02, 0x02, 0x09,
    0x04, 0x0A, 0x0A, 0x08, 0x0A, 0x0A, 0x0B, 0x0C, 0x09, 0x0D, 0x0D, 0x0D, 0x0D, 0x0D, 0x0D, 0x05,
    0x05, 0x0D, 0x0D, 0x04, 0x0A, 0x0A, 0x0B, 0x04, 0x03, 0x04, 0x00, 0x00, 0x00, 0x00, 0x00, 0x01,
    0x04, 0x00, 0x00, 0x00, 0x0A, 0x0A, 0x0B, 0x05, 0x0D, 0x05, 0x07, 0x07, 0x07, 0x07, 0x07, 0x05,
    0x05, 0x05, 0x05, 0x04, 0x0A, 0x0A, 0x0B, 0x05, 0x05, 0x06, 0x0A, 0x0A, 0x0A, 0x08, 0x0B, 0x05,
    0x05, 0x06, 0x00, 0x03, 0x0C, 0x0A, 0x0A, 0x02, 0x01, 0x0E, 0x0A, 0x09, 0x0E, 0x00, 0x0B, 0x05,
    0x05, 0x0E, 0x00, 0x0B, 0x06, 0x0A, 0x0A, 0x09, 0x06, 0x09, 0x0E, 0x01, 0x0E, 0x00, 0x0B, 0x05,
    0x05, 0x0E, 0x00, 0x0B, 0x0C, 0x0A, 0x0A, 0x03, 0x0D, 0x06, 0x09, 0x05, 0x0E, 0x00, 0x0B, 0x05,
    0x05, 0x0E, 0x00, 0x0B, 0x06, 0x0A, 0x0A, 0x09, 0x05, 0x0D, 0x06, 0x01, 0x0E, 0x00, 0x0B, 0x05,
    0x07, 0x0E, 0x02, 0x0A, 0x0A, 0x0A, 0x0A, 0x02, 0x02, 0x02, 0x0A, 0x02, 0x0A, 0x02, 0x0B, 0x07,
])
```