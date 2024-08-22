# Snap2DQuake

BEFORE STARTING:
Snappy needs to be continuously updated, so if some steps explained in this READ.ME regarding the interpreter and environment setting give strong problems, the authors advice to download SNAP ESA software and to enable the option "Python" during the installing process (see:https://senbox.atlassian.net/wiki/spaces/SNAP/pages/2499051521/Configure+Python+to+use+the+new+SNAP-Python+esa+snappy+interface+SNAP+version+10) 
To download snaphu algorithm for phase unwrapping, visit the url https://step.esa.int/main/snap-supported-plugins/snaphu/
-------------------
UPDATE OF 15/05/2024: 
With the new upgrade of SNAP10, many things have changed. The module for using SNAP in Python is called "esa_snappy" and is in continuous upgrading. The features are more or less the same oft the old snappy, with the exception of the deprecation of ProductUtils (substituted with GeoUtils).

The configuration of  esa_snappy is a bit complex and you can find some tips on the page https://forum.step.esa.int/t/error-while-configuring-esa-snappy-with-python-3-9-13-on-windows-11-configuration-failed-no-error-code/42164

The steps I personally did to enable this new version are:
1) Creation of a new environment with Python 3.10.11 (the library works with this version of Python, or lower...)
3) Installation of SNAP software (IMPORTANT: use an installation folder outside "Users" - e.g., C:\esa-snap) enabling the option of SNAP-Python using the preferred python.exe. PERSONALLY: I use Anaconda, so I selected this Python: C:\Users\navre\anaconda3\python.exe
4) Please, delete any space from your paths. Rename the folders which contain spaces.
5) Open a cmd, move to the directory of anaconda3\condabin and digit conda.bat activate env (env = name of the environment you chose e.g. If your environment's name's snap4python, call: conda.bat activate snap4python)
6) Move to esa-snap\bin directory and digit snappy-conf.bat <path of the python.exe>
7) Now, opening python with the environment that you created, you should be able to do import esa_snappy.
8) If it's not possible, on 5) put the path of the python.exe from your environment and try the step 6)
9) When  running the environment, if there are problems with JVM, set "conda env config vars set JAVA_HOME="C:\Program Files\esa-snap\jre", and then, set "env config vars set SNAP_HOME="C:\Program Files\esa-snap"
10) Install in your environment all the libraries indicated in the code (e.g., pip install numpy)
11) Run the code

It's a bit confusing, but we're trying to work everyday on it to better understand the installation process. Regarding the code, after the correct importing of esa_snappy, the ONLY necessary modification step is the substitution of "snappy" with "esa_snappy".
PLEASE, DO NOT ESITATE TO CONTACT US FOR ANY ISSUE: martina.occhipinti@dottorandi.unipg.it
-------------------
UPDATE OF 22/08/2024:
esa_snappy has been updates to 10.1, beware on setting it up orrectly. If new in esa_snappy, consult the latest topics on this url https://forum.step.esa.int/t/error-while-configuring-esa-snappy-with-python-3-9-13-on-windows-11-configuration-failed-no-error-code/42164 to a better explanation of the installing process,since you do NOT neet to configure esa_snappy Python as for the previous versions. Some issues might be solved, but the necessary Python is still the 3.10 version. 

--------------------
This repository contains all the elements needed to run Snap2DQuake.
In the repository, the user can find:

a) Snap2DQuake script

b) xml_files folder

PRODUCTS:

a) Snap2DQuake file is the file containing the script, to directly copy-paste in your Python editor, and in which the user can find some instruction to know where to insert all the necessary input data.

b) .xml files contain the graphs in .xml format to reproduce some operators of SNAP without using snappy. These processes are automatic. .xml files will be downloaded authomatically with all the other products. The user must put all the .xml files into a fixed folder with a easy path, that will be the same for each case study the user will analyse.

The authors advice to download every item (ascending and descending products) and to send them in a main folder (related to the single case study) which path is short and easy to reach. Snap2DQuake will automatically separate them into ascending and descending. It's adviced to keep the data in the same hard disk where the installed products to run the script are.

![image](https://github.com/navre6/Snap2DQuake/assets/134698198/3ddadca9-ca74-4778-8bde-ea2e9c7c5fbb)

To start running the environment, from the Anaconda Home page select the enterpreter (the authors are used to Visual Studio Code), and open a folder where to place the script file. After the opening of the folder, create a new file (1), paying attention to use the ".py" at the end of the name to give the file the Python format. Then, open a new terminal (2), and on the right corner of the terminal click on the arrow corresponding to "Launch profile" (3) and open a Command Line. Then, authomatically the snap environment must run in the terminal. If it's not, the user must digit "conda activate snap" to launch it (4).

![Screenshot 2023-07-25 094400](https://github.com/navre6/Snap2DQuake/assets/134698198/2e635954-d3d2-4208-a0f9-b148de23bc2e)

An error that commonly occurs is the heading space. In that case, when the ascending part of processing is completed, you can delete the files in "ascending" folder, EXCEPT FOR THE TERRAIN CORRECTION.DIM AND .DATA (and the .tif, obviously!)
Any new update will be available in this README.md file
