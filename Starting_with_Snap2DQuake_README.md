# Snap2DQuake

BEFORE STARTING:
Snappy needs to be continuously updated, so if some steps explained in this READ.ME regarding the interpreter and environment setting give strong problems, the authors advice to download SNAP ESA software from the link indicated in the paper Occhipinti et al. (2024) and to enable the option "Python" during the installing process (see:https://senbox.atlassian.net/wiki/spaces/SNAP/pages/2499051521/Configure+Python+to+use+the+new+SNAP-Python+esa+snappy+interface+SNAP+version+10)
This will allow the user to have a new snap-python folder. 
To download snaphu algorithm for phase unwrapping, visit the url https://step.esa.int/main/snap-supported-plugins/snaphu/
-------------------
UPDATE OF 06/05/2024: With the new upgrade of SNAP10, the folder "snappy" is not containing useful files anymore, as for the environment. So please don't download it. The authors are providing the updated folder as soon as possible. The new module to use SNAP on Python is esa_snappy, which contains the same features of snappy. The configuration is a bit complex and you can find some tips on the page https://forum.step.esa.int/t/error-while-configuring-esa-snappy-with-python-3-9-13-on-windows-11-configuration-failed-no-error-code/42164
The steps I personally did to enable this new version are:
1) Creation of a new environment with Python 3.10.11 (the library works with this version of Python, or lower...)
2) Installation of SNAP software enabling the option of SNAP-Python using the preferred python.exe. PERSONALLY: I use Anaconda, so I selected this Python: C:\Users\navre\anaconda3\python.exe
3) Open a cmd, move to the directory of anaconda3\condabin and digit conda.bat activate [env] (env = name of the environment you chose)
4) Move to esa-snap\bin directory and digit snappy-conf.bat <path of the python.exe>
5) Now, opening python with the environment that you created, you should be able to do import esa_snappy.
6) If it's not possible, on 5) put the path of the python.exe from your environment and try the step 6)
7) When  running the environment, if there are problems with JVM, set "conda env config vars set JAVA_HOME="C:\Program Files\esa-snap\jre", and then, set "env config vars set SNAP_HOME="C:\Program Files\esa-snap"


It's a bit confusing, but we're trying to work everyday on it to better understand the installation process. Regarding the code, after the correct importing of esa_snappy, the ONLY necessary modification step is the substitution of "snappy" with "esa_snappy". ProductIO, and all the other features of the module are still available and the code doesn't need any customization.
-------------------

This repository contains all the elements needed to run Snap2DQuake.
In the repository, the user can find:

a) Snap2DQuake script

b) xml_files folder

c) snap.yaml

d) an example of a snappy.properties file

e) snappy folder, which contains all the features to execute Snap2DQuake


PRODUCTS:

a) Snap2DQuake file is the file containing the script, to directly copy-paste in your Python editor, and in which the user can find some instruction to know where to insert all the necessary input data.

b) .xml files contain the graphs in .xml format to reproduce some operators of SNAP without using snappy. These processes are automatic. .xml files will be downloaded authomatically with all the other products. The user must put all the .xml files into a fixed folder with a easy path, that will be the same for each case study the user will analyse.

c) snap.yaml is the environment in which run Snap2DQuake. To work with this environment, the user must download Anaconda (https://www.anaconda.com/), and after the installation, go in the "Environments" section and click on "Import": then, choose the snap.yaml file. In this way, the environment will be imported.

d-e) The authors strongly advice to the user to insert snappy folder and snappy properties file in a same folder, to call "snap-python", but to keep the .txt file and the folder separated. (look to the image below)

![image](https://github.com/navre6/Snap2DQuake/assets/134698198/6055817a-cd0c-48d7-922c-eb13cb659fb7)


The authors advice to download every item (ascending and descending products) and to send them in a main folder (related to the single case study) which path is short and easy to reach, and to create two empty folders called "ascending" and "descending" inside the main folder. (look to the image below). It's adviced to keep the data in the same hard disk where the installed products to run the script are.

![image](https://github.com/navre6/Snap2DQuake/assets/134698198/3ddadca9-ca74-4778-8bde-ea2e9c7c5fbb)

To start running the environment, from the Anaconda Home page select the enterpreter (the authors are used to Visual Studio Code), and open a folder where to place the script file. After the opening of the folder, create a new file (1), paying attention to use the ".py" at the end of the name to give the file the Python format. Then, open a new terminal (2), and on the right corner of the terminal click on the arrow corresponding to "Launch profile" (3) and open a Command Line. Then, authomatically the snap environment must run in the terminal. If it's not, the user must digit "conda activate snap" to launch it (4).

![Screenshot 2023-07-25 094400](https://github.com/navre6/Snap2DQuake/assets/134698198/2e635954-d3d2-4208-a0f9-b148de23bc2e)


Any new update will be available in this README.md file
