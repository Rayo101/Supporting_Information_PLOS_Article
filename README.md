# Supporting_Information_PLOS_Article
This repository contains all the supporting information associated with the PLOS One article discussing the ability of PEPT to reproduce high fidelity Lagrangian and Eulerian features.  

There are three folders which are True, Tracks_OL1 and Tracks_noOL1.  The True folder contains all the True paths in text format.  The first column is the time in seconds and the final 3 columns are the X, Y and Z locations in millimetres.  The Tracks_OL1 and Tracks_noOL1 folders contain the paths and optimal PEPT-ML tracking parameters.  To load the true paths simply use numpy.loadtxt("path_to_file", skiprows = 3).  You then need to filter out the relevant columns outlined.  

Within the Tracks_X (X can either be noOL1 or OL1) folder the paths are separated by their temporal step $\tau$ into multiple folders named TS_Yms where Y is the temporal step in milliseconds.  Within the respective Tracks_X folder there is also a OptVals.csv file which contains all the optimal PEPT-ML tracking parameters and other additional information such as location rate and path uncertainty.  

All tracked paths are saved as *.npy files which is a binary file format used by the python numpy package.  To load in the paths simply used numpy.load("Path_to_file").  The columns are ($t$ (s), $X$ (mm), $Y$ (mm), $Z$ (mm)).  
