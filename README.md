# AStarObstacleDetection
Obstacle Detection using A Star Algorithm

# Path Planning and Obstacle Detection

## Project Description
This project is focused on path planning, a critical aspect of navigation which involves finding the shortest and most efficient route between two points. It's designed to ensure that navigation is both time-efficient and energy-saving, providing an optimized approach to the task.

## Overview

The project works with a collection of test images, each illustrating a different scenario:

- **Grid Structure**: Each image contains a 10x10 grid, totaling 100 squares.
- **Obstacles**: Some squares are marked as obstacles and are represented as black squares.
- **Objects**: Each object in the grid is characterized by three attributes - shape, size, and color.

Each square is identified by coordinates `(x, y)`, where `x` is the column number and `y` is the row number. The squares can be empty, occupied by an obstacle, or contain an object.

## Key Outputs

1. **Occupied Grid Coordinates**:
   - The program returns a list of coordinates for occupied grids (those with either an obstacle or an object). This is presented as a list of tuples, where each tuple contains the `x` and `y` coordinates.

2. **Minimum Path Calculation**:
   - The program identifies the nearest matching object for each object in the test images using the `compare_ssim` function from `scikit-image`.
   - The shortest path for traversal between objects is computed using the A* search algorithm, considering only horizontal and vertical movements.
   - The output is a Python dictionary where:
     - Each key is a tuple representing the coordinates of an object.
     - The value is a tuple of three elements: 
       - The coordinates of the nearest object.
       - A list of tuples representing the route path.
       - The number of moves taken for traversal.


## Usage

- Run `main.py` to see the results. Modify the test image in `main.py` for different scenarios.
- `process_image.py` contains the core functionality. Review this script for the main logic.
- `astarsearch.py` implements the A* search algorithm.
- `traversal.py` deals with object detection and path calculation.

## Installation and Dependencies

Dependencies can be installed using pip ([installation guide](https://pypi.python.org/pypi/pip)):

1. **OpenCV**: [Windows Installation](http://docs.opencv.org/3.1.0/d5/de5/tutorial_py_setup_in_windows.html) | [Ubuntu Installation](http://www.pyimagesearch.com/2015/06/22/install-opencv-3-0-and-python-2-7-on-ubuntu/)
2. **scikit-image**: Run `pip install scikit-image` in the command prompt.
3. **NumPy**: Run `pip install numpy` in the command prompt.
