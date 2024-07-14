Tetrahedron Visualization

This repository contains code to visualize a rotating tetrahedron using Python's matplotlib and scipy.spatial libraries.
Overview

This project demonstrates how to create a 3D visualization of a tetrahedron and animate its rotation. The code generates a GIF of the rotating tetrahedron.
Dependencies

Ensure you have the following Python libraries installed:

    numpy
    matplotlib
    scipy
Code Explanation

The script defines the vertices of a tetrahedron, computes its convex hull, and creates an animation of the rotating tetrahedron. The key components of the code are:

    Vertices Definition: Defines the four vertices of the tetrahedron.
    Convex Hull Calculation: Uses scipy.spatial.ConvexHull to compute the convex hull.
    Visualization: Uses matplotlib to create a 3D plot and animate the rotation.

Output

The script produces a GIF named tetrahedron_rotation.gif that shows a 360-degree rotation of the tetrahedron.
Usage

Run the script in a Python environment to generate the rotating tetrahedron GIF:
