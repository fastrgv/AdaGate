![screenshot](https://github.com/fastrgv/AdaGate/blob/master/shortFB.gif)
![screenshot](https://github.com/fastrgv/AdaGate/blob/master/palm.gif)
![screenshot](https://github.com/fastrgv/AdaGate/blob/master/adagate.jpg)
![screenshot](https://github.com/fastrgv/AdaGate/blob/master/atollNight.jpg)

Where is the source code?  Developers read this:

https://github.com/fastrgv/AdaGate/blob/master/sourceCode.txt


# AdaGate
AdaGate is a first-person 3D sokoban puzzle game within a Stargate / Portal fantasy setting that runs on Windows, Mac OS-X and GNU Linux.

Click on the most recent large 7z file under releases to download all source & binaries (Win/Mac/Linux), or try this link:

https://github.com/fastrgv/AdaGate/releases/download/v7.3.0/ag6nov20.7z




===========================================================================================


newest kawoosh video:  https://youtu.be/Wm-x_6W1fXI

SokobanDuke Video:  https://youtu.be/qgY8vF-bb8A

FireBall Video:  https://github.com/fastrgv/AdaGate/blob/master/fireball.flv

Duke&ZPM Video:  https://youtu.be/rIen-9oAQ2I

LavaPool Video: https://youtu.be/FnUv9EW4bZs 

Shark/Snake/Kawhoosh:  https://youtu.be/88Y4yvdixY4



# AdaGate GLFW/OpenAL version

## Recent Changes


**ver 7.3.0 -- 07nov20**
* Installed completely new cross-platform sound system using OpenAL.
* Revised sounds for event horizon & lava pool, lava pool speedup.

## More change-history at end of file.


## AdaGate Game Description
AdaGate is a strategy game with escape rooms in a Stargate fantasy setting. It is an elaborate example of modern OpenGL programming using the Ada language; and a tribute to Narbacular Drop.

Runs on Windows, OSX, and GNU/Linux.  The linux binary now runs on many linux distros!

While searching a remote south-seas atoll for remnants of a lost American heroine, you find a nearly operational stargate.  If you can get it working, you will be transported into an off-world temple with multiple chambers.  You'll need to power up the portal system by rolling alien power cells onto their sockets.  Simple, right?  Then use your portal gun to bypass obstacles through another dimension.

Escape all chambers to ascend to the lake sanctuary, where the level of difficulty is increased for your next game.



## AdaGate Game Features

* Works on PCs or laptops running Windows, OSX or GNU/Linux.  And if GNAT is installed you can rebuild it yourself!  But first try the binaries that are delivered for all platforms.

* Full source is provided.

* Note that a 64 bit build for Windows is delivered.

* Laptop friendly controls;  supports Mac Retina displays.

* A 3D Sokoban puzzle game that uses the intersection of two cylinders as a puzzle piece that rolls in two perpendicular directions.

* New stargate dial-home-device [DHD] allows non-linear play; see the island setting evolve from sun to fog to evening to night.

* Roll the ZPM power cells to empower the portals and escape thru a wormhole

* Four rooms and five degrees of difficulty for a total of 20 challenging puzzles. And solutions are available in the file ./data/solns.sok.

* Serves as a blueprint for modern OpenGL programming in Ada or C++ using GLSL 330, shaders, uniforms and textures.

* Note that Sangwine's PNG-IO library, and the Ada bindings to OpenAL, OpenGL & GLFW3 in this app constitute a complete, yet easily extendable Ada library that could be used for most any modern OpenGL project including games, animations, simulations, modeling, or engineering.

* The new sound system enables a build with surprising portability across various linux distros, as well as across various platforms.



## mouse/touchpad/keyboard controls

[You might need to disconnect unused gamecontrollers to prevent spinning!]

Look direction is controlled by touch pad or mouse;
The mouse wheel controls camera zoom.  On MacBooks, a 2-finger swipe simulates the mouse wheel.  Zoom can also be controlled with keys n, f, z [Nearer,Further,default];

Movement is controlled by the WASD keys or the arrow keys:

			(Up)
	(Lt)	(Dn)	(Rt)

Shoot the two portal guns using:  (L)-key (R)-key, or (if you have two) the two mouse buttons.

(space)-key => jump up/over short walls

(esc)-key => exit;

* (m)-key or (F1)-key	=> toggle between mouse-view (1st-person) or avatar(3rd-person)

In case of control problems with the game, or if you want to easily inspect something, use 1st-person mode.


### joystick
* joystick : attitude
* center thumb btn: forward
* trigger btn: backward
* Ltop/Rtop btns: select/shoot
* 1st base btn: jump

------------------------------------------------------------
### gamecontroller
* Lpaddle/Lhat : attitude
* Rpaddle : movement
* L/R Shoulder btns: select/shoot
* 1st Dpad-down btn: jump

------------------------------------------------------------
### controller settings
If the need arises, copy the file "default_settings.txt" to "settings.txt".  Then you can manually edit the floats that define the sensitivity for mouse, keyboard, gamepad & joystick, as well as forward speed of the avatar.

------------------------------------------------------------

If you ever get stuck, try to jump up + forward or back.

------------------------------------------------------------
------------------------------------------------------------


## required for running:

* graphics card with ample memory & updated driver that supports OpenGL version 3.3 or later.  
* Windows, GNU/Linux or OSX;
* optional game controller or joystick.


### Note on Intel embedded graphics
* Such hardware uses system RAM;  8Gb is enough to run but the drivers I've experienced exhibit annoying flaws, although the game is still playable.


## Setup & Running Adagate:

The application's main directory [./agate/] contains files for deployment on 3 platforms:  1)windows, 2)OS-X, 3)linux, in addition to source code.  If you are NOT running windows, you do not need .dll files.  If you are NOT running OS-X, you do NOT need the subdirectory named ./adagate.app/.

Windows users see also:  "windows-setup.txt"
Mac users should read "osx-setup.txt".

Unzip the archive.  On Windows, 7z [www.7-zip.org] works well for this.

The game may be run from a command line terminal window on all 3 platforms. Navigate to the installation directory and type:

adagate.bat (Windows)
adagate_osx (Mac)
adagate_gnu (Linux)

----------------------------------------------------------------------

This linux executable was built on [RedHat] Scientific-Linux to not only run well, but to rebuild easily. I believe this single linux executable will run on most recent distributions of linux. It has been tested on OpenSuse and Mint.

But the distributed linux executable requires glibc v2.14 or newer.  That means if your distribution is an older one, it may not run, and you will need to recompile.

----------------------------------------------------------------------
Mac users may also initiate the game by navigating to the installation directory in Finder and clicking the "adagate.app" icon named "AdaGate".

----------------------------------------------------------------------

The install directory should contain a subdirectory named "data".  It contains shaders, skyboxes, sound and texture data, as well as the puzzle definitions.

Tips:  0) type "h" for the help screen.  1) the ZPM is heavy!  If you kick it out of reach under water then you will be stranded on the island.  2) when in trouble in a dungeon, jumping may help.

By the way, you are ideally supposed to solve the sokoban puzzles without jumping up onto the walls.  On the other hand, if you jump into the puzzle at the wrong place, it might be impossible to solve.

--------------------------------------------------------------------------
Notes:

First, note that your screen brightness might need to be reduced to fully appreciate the lighting effects in level 3.

Second, note that AdaGate is geared toward a fairly capable graphics card.

Third, note that this game runs fine on an Intel NUC with embedded Intel graphics, so the graphics demands are modest.

Fourth, note that adjustable OpenGL settings should favor performance.

--------------------------------------------------------------------------
Open source Ada developers are welcome to help improve or extend this game.

Please send improvements, comments, suggestions or questions to:

<fastrgv@gmail.com>

-------------------------------------------------------------------

## Open Source libraries included that allow rebuilding:
* GLFW3, glext
* the included "bindings" directory contains Ada interfaces:
	* AdaPngLib
	* gl
	* glfwada
	* OpenAL

## Rebuild Requirements:
* systems:  Windows, OSX or GNU/Linux
* a recent GNAT-GPL Ada compiler from AdaLibre
* Xcode g++ compiler, if using OSX

Note that the module that defines the Ada interface to SFML-AUDIO, snd4ada.ads, was created with the command: "g++ -c -fdump-ada-spec -C snd4ada.hpp" which references a minimalistic C++ utility snd4ada.  Thus, if you redefine the interface snd4ada.hpp, you will need to recreate the interface spec snd4ada.ads by this method.

The audio system for the linux build, on the other hand, does not use SFML but its interface is identical.  It is portable but crude, since it needs an accurate duration value for any sound loops used.




## Build instructions for AdaGate:

Three [pre-compiled] binary executables are delivered, one for Windows, one for gnu/linux and one for OSX.  I think the Windows executable is fairly portable.  It was built on Windows 10 in 64-bit mode.  The Mac binary should run on most any standard Mac with a recent version of OSX.  The linux binary, adagate_gnu, is intended to run in the presence of the directory "./libs/gnu", which contains GLFW3 libraries that can be, but need not be present on a target system.

The distributed linux executable requires glibc v2.14 or newer.  That means if your distribution is older than june 2011, it may not run, and you will need to recompile.

Build scripts for GNAT-GPL 2015 or newer are provided;  and due to a recent script change, a Windows or linux build machine need not have a C++ compiler installed.  Only GNAT-GPL from AdaLibre is required (GNAT has its own g++).

-------------------------------------------------------

**msWin64** => wcmp.bat

Note that the above windows built scripts might need to be adjusted to reference your actual installation directory for 32bit AdaCore 2017 or 64bit AdaCore 2018 compilers.


-------------------------------------------------------
**MacOSX** => ocmp.sh

build script for generating a portable executable that will run on most OSX platforms whether or not they have non-standard libraries GLFW installed.  This is used to build the executable named adagate_osx.  Macs with a recent but standard configuration of OSX should be able to rebuild using this script, assuming you have GNAT GPL installed, as well as g++ from Xcode.

------------------------------------------------------
**GNU/Linux** => lcmp.sh

utilizes the shared GLFW libraries that are delivered in this bundle under ./libs/gnu/.  This is used to build the [gnu/linux] executable, which should run in the presence of ./libs/gnu/, whether or not your system has those shared libraries installed.

If the delivered linux binary does not run, try...

* Manually install GNAT GPL from libre.adacore.com/download/.
* Rerun the compile script lcmpd.sh.

### Fixable Linux Link Problems:

On a linux build machine, you might get fixable link errors, depending on its configuration.  If you are missing "libxxx.so", you might need to create a proper softlink so it can be found.


----------------------------------------------------------------------
## For Developers Only:  Portable Avatar Using Shaders

* This approach encapsulates the details of avatar shape, color, and movement within GLSL shaders and a related code object that defines vertices and texture maps.  The object may be an Ada package or C++ class.

* Programmatic inputs include uniforms for time, position, attitude, & type of motion.  The shaders then offload the realtime computational burdens onto the graphics processor.

* Data that defines shape and color, as well as the uniforms and functions that define behavior, reside completely within the object and shaders.  This data can ultimately be as detailed and refined as your imagination permits.  And any refinements made are not obfuscated in some esoteric or proprietary format with a limited audience, but remain fully portable and easily enhanced by most any developer using Free Open Source languages, tools and compilers.

* One approach would be to completely define the avatar within the shaders alone, possibly without using any texture files.  Just look at the creatures in (glslsandbox.com).  This would require advanced GLSL skills.

* But a huge selection of available MineCraft skins lead to the present avatar object design.

* In this application, the texture object is a cube with radius one that is defined as 6 disjoint cubelets (the precise name is rectangular cuboid or parallelpiped).  The 2 upper quarters map to the head and torso.  The lower half is divided into 4 cubelets that are mapped to arms and legs. See "cuboid.txt". The Minecraft images used for the texture also have 6 parts that map to the limbs, head and torso.

* The result is an utterly portable avatar defined by an image and 4 text files:
	* texture object body, avatarobj.adb
	* texture object specification, avatarobj.ads
	* vertex shader, avatarobj.vs
	* fragment shader, avatarobj.fs
	* any MineCraft Skin png file

* Interfacing game code with such an avatar is simple.  Essentially you need only pass the current uniform values prior to drawing, including time, position, attitude, motion-type.

* Of course one still needs a decent camera positioning and pointing policy within the game code in order to fully appreciate and exhibit the avatar. The details are beyond the scope of this brief introduction, but generally the current policy is a damped and delayed move toward some fixed ideal camera position above and behind the avatar.



----------------------------------------------------------------------
## For Developers Only:  Fancy Shaders

This app demonstrates how to use fancy fragment shaders from glslsandbox.com to make wormhole effects, starry skies, and moving-scene wall hangings. See below (Media Files).  It also demonstrates metallic texture overlays, and the use of coherent noise to create the stargate event horizon, and rolling fireball in the brick dungeon.


----------------------------------------------------------------------
## For Developers Only:  OpenAL portable sound package

This app uses a cross-platform sound-playing package for Ada apps that can asynchronously start and stop music loops, as well as initiate transient sounds.

It plays WAV files, via OpenAL, on Windows, OSX, and linux platforms.

It is suitable for any Ada application that needs music, sound loops or transient sound effects; eg. games.


----------------------------------------------------------------
----------------------------------------------------------------


## what is special about this project?

The linux-build of this app is among very few modern OpenGL games with sound where a single pre-built executable can run on multiple Linux distros without 3rd party add-ons! It has been tested on OpenSuse, ScientificLinux, Mint and CentOS. As mentioned earlier, the distributed linux executable requires glibc v2.14 or newer.  That means if your distribution is older than june 2011, you might need to rebuild.


For developers, this project can serve as a testbed for learning modern OpenGL and GLSL.

It uses the Ada programming language and modern OpenGL methods, with textures, shaders and uniforms.  Compiles and runs on Windows, GNU/Linux and Mac OSX systems.

Focusing on portability, transparency, and open source freedom, this project relies exclusively on F.O.S.S. tools:  a thin GLFW3 binding, a thin OpenGL binding, a PNG reader by Stephen Sanguine & Dimitry Anisimkov, OpenAL-Audio with a homebrew binding, and a GNAT compiler.

This is one of the most functionally advanced demonstrations of "modern" OpenGL using Ada to be published as a complete F.O.S.S. application.  The term "functionally advanced" means that the code is focused on comprehensibility and completeness rather than elegance.  Further development of structure and style is left as an exercise for the coding student.

The Ada bindings are thin, so the relationship to C++ methodology is transparent.  Developers should note that these Ada bindings can be used for any OpenGL Ada project.

For the C++ programmer the code should be easy to comprehend; and for the experienced Ada programmer there are many improvements to be made to better utilize the advanced protections and features of the Ada language.  

This is a work in progress, so please excuse any scaffolding and debugging code has not been removed.

If you make improvements, please send then to <fastrgv@gmail.com>





--------------------------
## License:


This app is covered by the GNU GPL v3 as indicated in the sources:


 Copyright (C) 2020  <fastrgv@gmail.com>

 This program is free software: you can redistribute it and/or modify
 it under the terms of the GNU General Public License as published by
 the Free Software Foundation, either version 3 of the License, or
 (at your option) any later version.

 This program is distributed in the hope that it will be useful,
 but WITHOUT ANY WARRANTY; without even the implied warranty of
 MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
 GNU General Public License for more details.

 You may read the full text of the GNU General Public License
 at <http://www.gnu.org/licenses/>.


## Media Files for AdaGate:

### General Note
The particular choices of sound, image, and fragment shader files [x.fs] delivered are not essential to the function of the game and are easily replaced.  This software is primarily intended as a tutorial example of modern OpenGL methods using GLSL.  The only requirements are that sounds be in WAV or OGG format, images be in PNG format, and shaders be updated to GLSL 330 specifications.  Skybox images must have a 90x90 degree field of view [for a correct perspective], and all 6 must have the same pixel dimensions.

### Defining Your Own Puzzles:
  Read puzzle_replacement.txt

### SoundFiles
Using "sox", most sounds have recently been converted to the WAV format.  Most sounds are from freesound.org and are covered by the Creative Commons Attribution noncommercial license documented in the accompanying file ccnc3_license.txt.  see also:  (http://creativecommons.org/licenses/by-nc/3.0/legalcode/)

See also: https://wiki.creativecommons.org/wiki/License%20Versions

"Among the Falls" [music for level 1], and others, are from (http://www.freesfx.co.uk).  See the file otherLicenses/freeSFX_license.txt.

OpiumLoop is from "PartnersInRhyme": see signed authorization in ~/otherLicenses/


### ImageFiles 
Most images for textures were freely [no copyright indications] available on google images.  Some wall textures used are from the GPL2.0/GPL3.0-only section of OpenGameArt.Org.  One other thatched roof texture was used from http://www.mayang.com/textures.  See mayang_license.txt.  Others from pixabay.com have a CC0 license.  More recently, some are from http://all-free-download.com/free-photos/.

### ShaderFiles 
Several fragment shader files used were downloaded from http://glslsandbox.com/ and put under ./data/.  All frag. shaders from glslsandbox are under the MIT license (see mit_license.txt).  Existing comments or any identifying information was retained.  What follows are acknowledgments for some that were identifyable.

Volcano & "Red Planet" from Mahmud Yuldashev <mahmud9935@gmail.com>, and "waterWorldCCNSA3.fs" with a CreativeCommons license, and which seems to be credited to Alexander Alekseev with mods by Mahmud Yuldashev.

In order to make any of these usable, I had to modernize them to glsl version 330 specifications, and adapt some to utilize additional uniforms for input.

### Avatars
Several are available under the directory ~/data/avatars/.  Simply copy your preferred one into ~/data/ and rename to skin.png.  Also, many other MineCraft avatars can be used.

### SkyBoxes 
For some of these, I lowered the horizon slightly for technical reasons;  and for others I converted to png files.

One source is (www.custommapmakers.org/skyboxes.php), which gathers together many free-to-use skyboxes.

Another skybox  [from  (http://www.redsorceress.com/skybox.html)]  is credited to "The Mighty Pete" at http://www.petesoasis.com (which seems defunct).

At least 3 beautiful hi-res skyboxes used [from OpenGameArt.org] are the work of Heiko Irrgang <hi@93-interactive.com> and is licensed under the Creative Commons Attribution-ShareAlike 3.0 Unported License.  To view a copy of this license, visit (http://creativecommons.org/licenses/by-sa/3.0/) or send a letter to Creative Commons, 444 Castro Street, Suite 900, Mountain View, California, 94041, USA.  See also the accompanying file ccsa3_license.txt.




## Best Download Sites for AdaGate and my other games:

https://github.com/fastrgv?tab=repositories

http://www.indiedb.com/members/fastrgv/games

https://fastrgv.itch.io/


## video links [all showing older versions of AdaGate]:

level beta puzzle:
<http://youtu.be/WQU5kdO_93k>

level beta lava pit:
<http://youtu.be/0LH9H0hNF1Q>

prolog flyover (dec15):
<http://youtu.be/IOybN0lgBh8>

agnew, atoll sea life (dec15):
<http://youtu.be/SZsdmISNia4>


A 3rd party 11 minute video of AdaGate is here:
<https://www.youtube.com/watch?v=qNPc6yXfIV4&feature=youtu.be>

Ominous Fireball (12mar17):
<https://youtu.be/iJnz_u3tsnY>

Duke goes for a swim (31oct17):
<https://youtu.be/D3yBovxkhGI>

----------------------------------------------------------------
----------------------------------------------------------------

## Older Change History:

**ver 7.2.0 -- 18sep20**
* Updated all glfw libs to v3.3.2.
* Added Windows launcher adagate.bat.

**ver 7.1.9 -- 25may20**
* Ceiling portals now allowed in level 2 [as well as 3].
* Floor portals allowed in any level.
* Updated music in level 3.


