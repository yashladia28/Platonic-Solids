Tetrahedron Visualization

This repository contains code to visualize a rotating tetrahedron using Python's matplotlib and scipy.spatial libraries.
Overview

This project demonstrates how to create a 3D visualization of a tetrahedron and animate its rotation. The code generates a GIF of the rotating tetrahedron.
Dependencies

Ensure you have the following Python libraries installed:

    numpy
    matplotlib
    scipy

You can install these libraries using pip:

sh

pip install numpy matplotlib scipy

Code Explanation

The script defines the vertices of a tetrahedron, computes its convex hull, and creates an animation of the rotating tetrahedron. The key components of the code are:

    Vertices Definition: Defines the four vertices of the tetrahedron.
    Convex Hull Calculation: Uses scipy.spatial.ConvexHull to compute the convex hull.
    Visualization: Uses matplotlib to create a 3D plot and animate the rotation.

python

import numpy as np
import matplotlib.pyplot as plt
from mpl_toolkits.mplot3d.art3d import Poly3DCollection
from matplotlib.animation import FuncAnimation
from scipy.spatial import ConvexHull

# Define tetrahedron vertices
points = np.array([[1, 1, 1], [1, -1, -1], [-1, 1, -1], [-1, -1, 1]])

# Calculate the convex hull
hull = ConvexHull(points)

# Create a 3D plot
fig = plt.figure()
ax = fig.add_subplot(111, projection='3d')

# Remove axes
ax.axis('off')
ax.grid(False)
ax.set_xticks([])
ax.set_yticks([])
ax.set_zticks([])

def init():
    # Add faces
    faces = Poly3DCollection([hull.points[simplex] for simplex in hull.simplices], alpha=0.5)
    faces.set_facecolor('c')
    ax.add_collection3d(faces)
    
    # Add edges
    for simplex in hull.simplices:
        s = hull.points[simplex]
        s = np.vstack((s, s[0]))
        ax.plot(s[:, 0], s[:, 1], s[:, 2], "k-")
    
    return faces,

def update(frame):
    ax.view_init(elev=10, azim=frame)
    return ax,

# Create and save the animation
anim = FuncAnimation(fig, update, frames=np.arange(0, 360, 1), init_func=init, blit=False)
anim.save('tetrahedron_rotation.gif', writer='imagemagick')

Output

The script produces a GIF named tetrahedron_rotation.gif that shows a 360-degree rotation of the tetrahedron.
Usage

Run the script in a Python environment to generate the rotating tetrahedron GIF:

sh

python tetrahedron_visualization.py

License

This project is licensed under the MIT License.

Feel free to modify the content as needed for your specific requirements.
