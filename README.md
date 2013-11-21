From nothing to a working windows mangos server
---
[![](page1.gif)](http://www.getmangos.co.uk)
[![](page2.gif)](page2.md)


###Part 1 - Downloading and Installling the required software
1. Install the OS - Either on a real PC or in a Virtual Machine

	Some prebuilt VM's can be obtained from microsoft at this location [http://www.modern.ie/en-US/virtualization-tools#downloads](http://www.modern.ie/en-US/virtualization-tools#downloads "HERE"). For this guide we are going to use the IE9 for Windows 7 VM.

2. Start to the OS and then download the following software onto a location in the VM:-

    [Microsoft Visual Studio](http://www.visualstudio.com/en-us) - We used 'Express Visual Studio 2013 for Windows Desktop'

    [Bzip2 library](http://sourceforge.net/projects/gnuwin32/files/bzip2/1.0.5/bzip2-1.0.5-setup.exe/download?use_mirror=netcologne&download=)

    [ZLib](http://sourceforge.net/projects/gnuwin32/files/zlib/1.2.3/zlib-1.2.3.exe/download?use_mirror=garr&download=)

    [ACE v6.0.8](http://download.dre.vanderbilt.edu/previous_versions/ACE-6.0.8.zip)

	[MySQL 5.5 Community Edition](http://dev.mysql.com/downloads/mysql/5.5.html#downloads) - Direct Links:  [32 Bit](http://dev.mysql.com/get/Downloads/MySQL-5.5/mysql-5.5.34-win32.msi)   /    [64 Bit](http://dev.mysql.com/get/Downloads/MySQL-5.5/mysql-5.5.34-winx64.msi) 

    [OpenSSL](http://slproweb.com/download/Win32OpenSSL-1_0_1e.exe) - You may also need the C++ 2008 Redist Libraries:  [32 Bit](http://www.microsoft.com/downloads/details.aspx?familyid=9B2DA534-3E03-4391-8A4D-074B9F2BC1BF) / [64 Bit](http://www.microsoft.com/downloads/details.aspx?familyid=bd2a6171-e2d6-4230-b809-9a8d7548c1b6)

    [CMake](http://www.cmake.org/files/v2.8/cmake-2.8.12.1-win32-x86.exe)

    [GIT](http://git-scm.com/download/win)
 
3.  Now the time consuming part, installing the downloaded software

	**OpenSSL** - If this mentions that you need the C++ 2008 libraries, install them then continue this installation. Most of the install screens use the default settings, except for the 'Additional Tasks' Screen. On this screen with the prompt 'Copy OpenSSL DLLs to:', Select 
    
        'The OpenSSL binaries (/bin) directory) option. 
    and on the last screen
        
        Untick the donate button, unless you intend to donate ;)

	**Bzip2** - Most of the install screens use the default settings, except for the 'Additional Tasks' Screen. On this screen with the prompt 'Additional icons:'

        Tick 'Download Sources' checkbox. 
	
	**ZLib** - Most of the install screens use the default settings, except for the 'Additional Tasks' Screen. On this screen with the prompt 'Additional icons:',         

        Tick 'Download Sources' checkbox. 

	**CMake** - A couple of options require changing during the install.

	    Select the option 'Add CMake to the system PATH for current user'. 

		Also tick the checkbox for creating a desktop icon

	**GIT** - A Few options need changing during the install.

        Select the option 'Run GIT from the Windows Command Prompt'

	**Visual Studio** - On this VM which has IE9, VS displays a warning, just click continue to ignore it.

    and finally....

     **MySQL** - When prompted for the install type, select 'Complete'. Once the install has completed it will start the 'MySQL Server Instance Configuration Wizard'. Generally select all the default options apart from the following:-

	    Tick the checkbox 'Add Firewall exception for this port'
	    Tick the Checkbox 'Include Bin Directory in Windows PATH'
	    Fill in the Root password and make a note of it somewhere
        Also tick the checkbox 'enable root access from remote machines'

	At this point, take a short break and relax, it gets much easier from now on.

[**Part 2 - Setting up the build environment**](MangosZero%2018.1%20Build%20Part%202) 

[**Part 3 - Downloading the Source and building it**](MangosZero%2018.1%20Build%20Part%203)
