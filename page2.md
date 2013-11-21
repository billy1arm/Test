From nothing to a working windows mangos server
---
[![](page1.gif)](page1.md)
[![](page2sel.gif)](page2.md)
[![](page3.gif)](page3.md)
###Part 2 - Setting up the build environment
**Zlib**
The default ZLib installation has an error which needs to be corrected. Locate the file `zconf.h` (normally in `program files\gnuwin32\include\`) and edit it (I would advise wordpad rather than notepad here). To find the line, just search for `#if 1`   
**NOTE**: The editing application wordpad etc. must be started as administrator to be allowed to save this file in the above location.

The line reads:

    #if 1                      /* HAVE_UNISTD_H ...the rest of the line

but should read

    #if HAVE_UNISTD_H /* ...the rest of the line


**ACE**

Open the folder where you downloaded `ACE 6.0.8.zip`

Extract the Zip file into a folder called the same name.

Navigate into this folder and then move into the `ace_wrappers\ace` subfolder.

In this folder create a file called `config.h` (make sure that it is created as a .h file and not .h.txt), open this file and add the following line to it:-

    #include "ace/config-win32.h"
Save this file, the move back up a folder level to `ace_wrappers`.  
Open the `ACE_wrappers_vcXX.sln` file for the version of VS you are using.

**NOTE**: For Visual Studio 2010/2012 or 2013 use the _vc10 one.

In the Solution Explorer Window right click on ACE, then select Build. Do this for both Debug and Release configurations.

Create the folders `Program Files/ACE/6.0.8`

Create a subfolder under 6.0.8 called `include` and copy the `ACE` folder from the `ace_wrapper` folder into it.

Now copy the `lib` and `bin` folders in `ace_wrappers` to folder `Program Files/ACE/6.0.8`

Congratulations, that is the build environment configured. You will not have to do the above steps again unless you are installing your OS :D

[**Part 1 - Downloading and Installling the required software**](MangosZero%2018.1%20Build%20Part%201) 

[**Part 3 - Downloading the Source and building it**](MangosZero%2018.1%20Build%20Part%203) 
