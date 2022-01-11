layout: post
title: "obtaine"
categories: misc
tag: 
  - misc

Obtaining volume, centre of gravity and inertia matrix from STL file

In order to get the details about the volume, centre of gravity and inertia matrix from the STL file of the geometry, we use the `numpy-stl` python library. It is an efficient and simple library to make work with STL files. The installation of this library is done using command:
`*pip install numpy-stl*`
After installing this package, we are ready to work with the STL files. Now, in order to evaluate the mesh properties like volume, centre of gravity and inertia, use the following command lines:



`import numpy as np from stl import mesh # Using an existing closed stl file: your_mesh = mesh.Mesh.from_file('file_name.stl') volume, cog, inertia = your_mesh.get_mass_properties() print("Volume                                  = {0}".format(volume)) print("Position of the center of gravity (COG) = {0}".format(cog)) print("Inertia matrix at expressed at the COG  = {0}".format(inertia[0,:])) print("                                          {0}".format(inertia[1,:])) print("                                          {0}".format(inertia[2,:]))`

