# 🎨 OpenGL with Python - Practical Tutorial

This repository contains practical examples of OpenGL using Python and PyOpenGL, developed for the Computer Graphics course.

## 📋 Pre-requisites

### Installing PyOpenGL
```bash
pip install PyOpenGL PyOpenGL-accelerate
```

### For Linux (Ubuntu/Debian) systems:

```bash
sudo apt-get install freeglut3-dev
```

### For macOS systems:

```bash
brew install freeglut
```

## 🚀 How to Run

Each example can be executed directly:

```bash
python basic_example.py
python exercise_01.py
# ... and so on
```

## 📚 Repository Structure

### Basic Examples

* `basic_example.py` - Creating an OpenGL window
* `basic_triangle.py` - Drawing a triangle
* `circle.py` - Drawing circles

### Practice Exercises

* `exercise_01.py` - Centroid and lines
* `exercise_02.py` - Circle algorithms
* `exercise_03.py` - Geometric transformations
* `exercise_04.py` - User interactions
* `exercise_05.py` - Animations (screensaver)

## 🎯 Covered Concepts

### 1. **Window Setup**

* GLUT initialization
* Window creation
* Coordinate system

### 2. **Projection System**

OpenGL uses a normalized coordinate system from -1 to 1 on each axis. The `gluOrtho2D()` function defines the visible area:

python
gluOrtho2D(-1.0, 1.0, -1.0, 1.0)  # Defines the visible area from -1 to 1 on X and Y


### 3. **Basic Primitives**

* `GL_POINTS` - Points
* `GL_LINES` - Lines
* `GL_TRIANGLES` - Triangles
* `GL_POLYGON` - Polygons

### 4. **Geometric Transformations**

* **Translation**: Moves an object in space
* **Rotation**: Rotates an object around an axis
* **Scaling**: Changes the size of an object

### 5. **Interactions**

* Keyboard (normal and special keys)
* Mouse (clicks and movement)

### 6. **Animations**

* Timer functions
* Idle functions

## 🎮 Exercise Controls

### Exercise 4 - Interactions

* **Arrow keys**: Move the triangle
* **WASD**: Rotate on X and Y axes
* **Q/E**: Rotate on the Z axis
* **+/-**: Increase/decrease scale
* **ESC**: Exit

### Exercise 5 - Animation

* **Spacebar**: Pause/resume animation
* **R**: Reset position
* **ESC**: Exit

## 🔧 Basic Structure of an OpenGL Program

```bash
from OpenGL.GL import *
from OpenGL.GLUT import *
from OpenGL.GLU import *

def draw():
    glClear(GL_COLOR_BUFFER_BIT)
    # Your drawing code here
    glFlush()

def main():
    glutInit()
    glutInitDisplayMode(GLUT_SINGLE | GLUT_RGB)
    glutInitWindowSize(800, 600)
    glutCreateWindow("My Window")
    
    glClearColor(0.0, 0.0, 0.0, 1.0)  # Background color
    gluOrtho2D(-1.0, 1.0, -1.0, 1.0)  # Coordinate system
    
    glutDisplayFunc(draw)
    glutMainLoop()

if _name_ == "_main_":
    main()
```

## 💡 Important Tips

1. **Coordinate System**: By default, OpenGL uses coordinates from -1 to 1
2. **Vertex Order**: For triangles, use counter-clockwise order
3. **Colors**: RGB values should be between 0.0 and 1.0
4. **Performance**: Use `GL_TRIANGLES` for complex objects instead of `GL_POLYGON`

## 📖 Additional Resources

* [PyOpenGL Documentation](http://pyopengl.sourceforge.net/)
* [OpenGL Reference](https://www.opengl.org/sdk/docs/)
* [LearnOpenGL](https://learnopengl.com/) (Applicable concepts)

## 👥 PAE Monitor

* **Graciella Favoreto**: [graciellafavoreto@usp.br](mailto:graciellafavoreto@usp.br)

**Office hours**: 18:00 to 20:00 - Room 1-116 (GBDI Lab)

---

**Profa** Dra. Agma Juci Machado Traina

**Course**: Computer Graphics - ICMC/USP
