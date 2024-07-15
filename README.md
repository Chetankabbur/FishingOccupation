# FishingOccupation

# Fish Animation OpenGL Project

## Overview

This project is an OpenGL-based fish animation program. It includes rendering various graphical elements such as a sun, water, fish, and other objects. The fish can be animated to move clockwise based on user input. The project is developed in C++ using OpenGL and GLUT libraries.

## Features

- **Sun and Sky**: The background includes a sky and a sun.
- **Fish Animation**: Fish can be animated to move clockwise.
- **Interactive Controls**: User can interact with the animation using keyboard inputs.
- **Boat and Houses**: Additional elements like boats and houses are included in the scene.

## Prerequisites

To run this project, you need to have the following installed:

- [OpenGL](https://www.opengl.org/)
- [GLUT (OpenGL Utility Toolkit)](https://www.opengl.org/resources/libraries/glut/)

## Setup and Compilation

1. **Install OpenGL and GLUT**:
    - On Windows, you can download and install the libraries from their respective websites.
    - On Linux, you can use the package manager to install them:
      ```sh
      sudo apt-get update
      sudo apt-get install freeglut3 freeglut3-dev
      ```

2. **Clone the Repository**:
    ```sh
    git clone <repository_url>
    cd <repository_directory>
    ```

3. **Compile the Code**:
    - On Windows, you can use an IDE like Visual Studio.
    - On Linux, you can use the g++ compiler:
      ```sh
      g++ -o FishAnimation main.cpp -lGL -lGLU -lglut
      ```

## Usage

1. **Run the Executable**:
    ```sh
    ./FishAnimation
    ```

2. **Keyboard Controls**:
    - `F` or `f`: Display the main scene.
    - `R` or `r`: Reset the animation.
    - `Q` or `q`: Quit the program.
    - `S` or `s`: Stop the animation.
    - `T` or `t`: Rotate the fish.
    - `C` or `c`: Start the fish moving clockwise.
    - `N` or `n`: Another animation control.

3. **Mouse Controls**:
    - No specific mouse controls implemented. 

## Files

- `main.cpp`: Main source file containing the OpenGL code.

## Code Explanation

### Main Functions

- **display**: Main display function to render the scene.
- **sky**: Function to draw the sky.
- **sun**: Function to draw the sun.
- **water**: Function to draw the water.
- **boat**: Function to draw the boat.
- **fish1**: Function to draw the fish and animate it.

### Helper Functions

- **circle1, circle2**: Functions to draw circles (used for fish and other elements).
- **clockWise**: Function to animate the fish in a clockwise direction.
- **mykeys**: Keyboard interaction function.
- **mouse**: Mouse interaction function.
- **update**: Timer function for animating the water and fish.

### Example Code Snippet

```cpp
void sun() {
    sky();
    glColor3ub(225, 225, 51);
    glPushMatrix();
    glTranslatef(950, 700, 0.0);
    glutSolidTorus(1, 30, 100, 200);
    glPopMatrix();
}
```

## Future Improvements

- Implement more interactive controls.
- Add more fish with different colors and animations.
- Enhance the graphical elements for better visual appeal.

