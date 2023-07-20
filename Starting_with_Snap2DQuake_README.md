# Snap2DQuake

This repository contains all the elements needed to run Snap2DQuake.
In the repository, the user can find:
-Snap2DQuake script, to directly copy-paste in your Python editor, and in which the user can find some instruction to know where to insert all the necessary input data.
-xml_files folder, in which are contained the graph in .xml format to reproduces some operators of SNAP without using snappy. These processes are automatic.
-snap.yaml, the environment in which run Snap2DQuake
-an example of a snappy.properties file
-snappy folder, which contains all the features to execute Snap2DQuake, including snaphu.exe


The authors advice to download every item (ascending and descending products) and to send them in a main folder (related to the single case study) which path is easy to reach, and to create two empty folders called "ascending" and "descending" inside the main folder. (look to the image below)

![image](https://github.com/navre6/Snap2DQuake/assets/134698198/3ddadca9-ca74-4778-8bde-ea2e9c7c5fbb)


Moreover, the authors strongly advice to the user to insert snappy folder and snappy properties file in a same folder, to call "snap-python", but to keep the .txt file and the folder separated. (look to the image below)

![image](https://github.com/navre6/Snap2DQuake/assets/134698198/6055817a-cd0c-48d7-922c-eb13cb659fb7)


To make the snap.yaml environment available, import it on Anaconda.

Snappy needs to be continuously updated, so if it gives strong problems, the authors advice to download SNAP ESA software from the link indicated in the paper Occhipinti et al. (2023) and to able the option "Python" during the installing process.
This will allow the user to have a new snap-python folder. ATTENTION: THIS EVENTUAL NEW FOLDER DOESN'T HAVE TO SUBSTITUTE THE ONE UPLOADED IN THIS REPOSITORY, because this latter contains saphu.exe, that isn't available in SNAP ESA software!!!

Any new update will be available in this README.md file
