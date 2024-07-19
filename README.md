Platonic Solids Visualization

This repository contains a Jupyter notebook that generates and visualizes the five Platonic solids: Tetrahedron, Cube (Hexahedron), Octahedron, Dodecahedron, and Icosahedron. The visualizations are provided as static plots and animated GIFs showing rotations of each solid.
Contents

    solids.ipynb: Jupyter notebook containing the code to generate and visualize the Platonic solids.
    tetrahedron_rotation.gif: Animated GIF of the rotating Tetrahedron.
    cube_rotation.gif: Animated GIF of the rotating Cube (Hexahedron).
    octahedron_rotation.gif: Animated GIF of the rotating Octahedron.
    dodecahedron_rotation.gif: Animated GIF of the rotating Dodecahedron.
    icosahedron_rotation.gif: Animated GIF of the rotating Icosahedron.

Dependencies

To run the notebook, you need the following Python libraries:

    numpy
    matplotlib
    scipy

You can install these dependencies using pip:

bash

pip install numpy matplotlib scipy

Usage

    Clone the repository:

    bash

git clone https://github.com/your-username/platonic-solids-visualization.git
cd platonic-solids-visualization

Open the Jupyter notebook:

bash

    jupyter notebook Platonic_Solids.ipynb

    Run the notebook to generate the visualizations and save the animated GIFs.

Examples
Tetrahedron

Tetrahedron
Cube (Hexahedron)

Cube
Octahedron

Octahedron
Dodecahedron

Dodecahedron
Icosahedron

Icosahedron

Acknowledgments

The convex hull computation is powered by scipy.spatial.ConvexHull. The 3D plotting is done using matplotlib and mpl_toolkits.mplot3d. Animations are created with matplotlib.animation.FuncAnimation.
