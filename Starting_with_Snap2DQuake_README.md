# Snap2DQuake

This repository contains all the elements needed to run Snap2DQuake.
In the repository, the user can find:
-Snap2DQuake script, to directly copy-paste in your Python editor, and in which the user can find some instruction to know where to insert all the necessary input data.
-xml_files folder, in which are contained the graph in .xml format to reproduces some operators of SNAP without using snappy. These processes are automatic.
-snap.yaml, the environment in which run Snap2DQuake
-snappy.properties .txt file
-snappy folder, which contains all the features to execute Snap2DQuake, including snaphu.exe

The authors advice to download every item and to send them in folder which path is easy to reach;
Moreover, the authors strongly advice to the user to insert snappy folder and snappy.properties in a same folder, to call "snap-python", but to keep the .txt file and the folder separated.

To make the snap.yaml environment available, import it on Anaconda.

Snappy needs to be continuously updated, so if it gives strong problems, the authors advice to download SNAP ESA software from the link indicated in the paper Occhipinti et al. (2023) and to able the option "Python" during the installing process.
This will allow the user to have a new snap-python folder. ATTENTION: THIS EVENTUAL NEW FOLDER DOESN'T HAVE TO SUBSTITUTE THE ONE UPLOADED IN THIS REPOSITORY, because this latter contains saphu.exe, that isn't available in SNAP ESA software!!!

Any new update will be available in this README.md file
