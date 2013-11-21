From nothing to a working windows mangos server
---
[![](page1.gif)](page1.md)
[![](page2.gif)](page2.md)
[![](page3sel.gif)](page3.md)###Part 3 - Downloading the Source and building it

#####Downloading the source
Click on Start, then Computer

Select the C Drive.

Create a new folder called `MangosZero`

Right click on the folder and select `Git Bash` from the menu.

The command prompt style window will open and wait with a prompt “$”

Type: `git clone git://github.com/mangoszero/server.git`

Once complete, close the window

#####Building the Source

Open Cmake and for the box labelled 'Where the source is', select the folder `c:/MangosZero/server`

For the box labelled 'Where to build the binaries', Select the folder `c:/MangosZero/sourcefiles`

Click Configure, the first time you do this for a folder it will prompt you to create the output folder, click Yes.

When you are prompted to ‘Specift the generator for this project’, select the option  for the version of VS you are using:

- For VS2010, select Visual Studio 10
- For VS2012, select Visual Studio 11
- For VS2013, select Visual Studio 12

Click Finish

Once complete the main window should display some information with a red background.

**Note**: The field `CMAKE_INSTALL_PREFIX` specifies the installed server path, click this field and change to your required path.

Then Click on ‘Generate’

Close down cmake and navigate to `c:/MangosZero/sourcefiles`

Open up the VS solution as normal and build.

Once the build is complete, all the files you need are in folder xxxx

[**Part 1 - Downloading and Installling the required software**](MangosZero%2018.1%20Build%20Part%201) 

[**Part 2 - Setting up the build environment**](MangosZero%2018.1%20Build%20Part%202) 
