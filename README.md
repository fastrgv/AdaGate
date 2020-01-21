![screenshot](https://github.com/fastrgv/AdaGate/blob/master/palm.gif)
![screenshot](https://github.com/fastrgv/AdaGate/blob/master/adagate.jpg)
![screenshot](https://github.com/fastrgv/AdaGate/blob/master/atollNight.jpg)

Where is the source code?  Developers read this:

https://github.com/fastrgv/AdaGate/blob/master/sourceCode.txt


# AdaGate
AdaGate is a first-person 3D sokoban puzzle game within a Stargate / Portal fantasy setting that runs on Windows, Mac OS-X and GNU Linux.

Click on the most recent large 7z file under releases to download all source & binaries (both Mac & Linux), or try this link:

https://github.com/fastrgv/AdaGate/releases/download/v7.1.0/ag21jan20.7z




=====================================================================================================


newest kawoosh video:  https://youtu.be/Wm-x_6W1fXI

SokobanDuke Video:  https://youtu.be/qgY8vF-bb8A

FireBall Video:  https://github.com/fastrgv/AdaGate/blob/master/fireball.flv

Duke&ZPM Video:  https://youtu.be/rIen-9oAQ2I



# AdaGate GLFW version

## Recent Changes

**ver 7.1.0 -- 20jan20**

* Quantum improvement in linux portability by avoiding SFML libs.


**ver 7.0.4 -- 12jan20**

* Fixed ball of rolling magma.
* Settings files now allow Dos-Format.
* Updated to GLFW v3.3.1 (released 1jan2020).
* Updated Ada binding to GLFW331, also.
* Improved a few textures.
* Possibly enhanced portability of linux version game.

**ver 7.0.3 -- 09jan20**

* Improved handling of HiDpi on OSX;
* Improved controlability of mouse slew @ HiDpi.
* Added ~/data/settings.txt file to allow users to adjust:
	* Forward/Backward Speed
	* Slew Speed using:
		* keyboard
		* mouse
		* gamepad
		* joystick


**ver 7.0.2 -- 07jan20**

* Jumps were disabled, but have been fixed;
* Fixed interior drawing order problem causing objects to disappear;
* Improved windows build method;
* FTTB, OSX binaries run only @ HighDpi due to issues with GLFW3;
* Now delivering this GLFW version as the mainstream version;


**ver 7.0.1 -- 25dec19**

* Finalized code for basic joystick function.
* Finalized code for joystick/gamepad jump function (when not on beach).


**ver 7.0.0 -- 24dec19**

* Converted Ada code to use GLFW, rather than SDL2;
* Updated libraries, DLLs, Ada binding;
* Limited gamepad functionality;


**ver 6.5.4 -- 17dec19**

* Completed storyline with fleeting stargates at dungeon entries.
* Updated SDL2 to v2.0.10


**ver 6.5.3 -- 31nov19**

* Refined the measure that determines nearness to stargate event horizon, and triggers the wormhole traversal.
* Now deliver two executables for Mac/OSX, defaulted to Low-Dpi.


## More change-history at end of file.


## AdaGate Game Description
AdaGate is a strategy game with escape rooms in a Stargate/NarbacularDrop fantasy setting. It is a fully elaborated example of modern OpenGL programming using the Ada language that runs on Windows, OSX, and GNU/Linux.

While searching a remote south-seas atoll for remnants of a lost American heroine, you find a nearly operational stargate.  If you can get it working, you will be transported into an off-world temple with multiple chambers.  You'll need to power up the portal system by rolling alien power cells onto their sockets.  Simple, right?  Then use your portal gun to bypass obstacles through another dimension.

Escape all chambers to ascend to the lake sanctuary, where the level of difficulty is increased for your next game.



## AdaGate Game Features
* Works on PCs or laptops running Windows, OSX or GNU/Linux.  And if GNAT is installed you can rebuild it yourself!  But first try the delivered binaries.
* Windows, GNU/Linux and OSX binaries provided, as well as full source. 
* Note that both 32 and 64 bit builds for Windows are delivered.
* Laptop friendly controls;  supports Mac Retina displays.
* A 3D Sokoban puzzle game that uses the intersection of two cylinders as a puzzle piece that rolls in two perpendicular directions.
* New stargate dial-home-device [DHD] allows non-linear play; see the island setting evolve.
* Roll the ZPM power cells to empower the portals and escape thru a wormhole
* Four rooms and five degrees of difficulty for a total of 20 challenging puzzles. And now solutions are available in the file ./data/solns.sok.
* Serves as a blueprint for modern OpenGL programming in Ada or C++ using GLSL 330, shaders, uniforms and textures.
* Note that Sangwine's PNG-IO library, and the Ada bindings to SFML, OpenGL & SDL2 in this app constitute a complete, yet easily extendable Ada library that could be used for most any modern OpenGL project including games, animations, simulations, modeling, or engineering.




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

* (m)-key or (F1)-key	=> toggle mouse-view (1st-person) or avatar(3rd-person)

In case of control problems with the game, or if you want to easily inspect something, temporarily switch to 1st-person mode.


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
If the need arises, copy the file "default_settings.txt" to "settings.txt".  Then you can manually edit the integers that define the button-bindings or the floats that define the sensitivity.

------------------------------------------------------------

If you ever get stuck, try to jump up + forward or back.

------------------------------------------------------------
------------------------------------------------------------


## required for running:

* graphics card with ample memory & updated driver that supports OpenGL version 3.3 or later.  
* Windows, GNU/Linux or OSX;
* optional game controller or joystick.


### Note on Intel embedded graphics
* Such hardware use system RAM;  8Gb is enough to run but the drivers I've experienced exhibit annoying flaws, although the game is still playable.


## Setup & Running Adagate:

The application's main directory [./agate/] contains files for deployment on 3 platforms:  1)windows, 2)OS-X, 3)linux, in addition to source code.  If you are NOT running windows, you do not need .dll files.  If you are NOT running OS-X, you do NOT need the subdirectory named ./adagate.app/.

Windows users see also:  "windows-setup.txt"
Mac users see "osx-setup.txt".

Unzip the archive.  On Windows, 7z [www.7-zip.org] works well for this.

Open a commandline terminal, and cd to the install directory.  If your platform is High-Dpi-capable, type the executable-name followed by a "1", before hittting the (enter-key).  But if the game does not play smoothly, you should run in Low-Dpi mode.

Linux users should type "adagate_gnu" to start the game.  You may also double click its icon in file manager.

Similarly, Mac users may initiate the game by navigating to the installation directory in Finder and clicking the "adagate.app" icon named "AdaGate".

Windows users type either a) "binw32\adagate32.exe" or b) "binw64\adagate64.exe" from the install directory.


The install directory should contain a subdirectory named "data".  It contains shaders, skyboxes, sound and texture data, as well as the puzzle definitions.

An optional command line parameter of 1..5 will choose the Degree-of-Difficulty [DOD], but it is normally unnecessary since the DoD increments itself after each game.  If you succeed at DoD= 3 or 4 then you are ready to try WorldCupSokerban or RufasSok!

Tips:  0) type "h" for the help screen.  1) the ZPM is heavy!  If you kick it out of reach under water then you will be stranded on the island.  2) when in trouble in a dungeon, jumping may help.

By the way, you are ideally supposed to solve the sokoban puzzles without jumping up onto the walls.  On the other hand, if you jump into the puzzle at the wrong place, it might be impossible to solve.

--------------------------------------------------------------------------
Notes:

First, note that your screen brightness might need to be reduced to fully appreciate the lighting effects in level 3.

Second, note that AdaGate is geared toward a fairly capable graphics card.  If you have graphical glitches during a wormhole passage, and you have an Ada compiler you can fix that.  So if your graphics card is old and less-capable, you should edit "src/gameutils-setup_textures.adb" to use lightweight shaders.  Search for "tunshadid" (near the end of the file).  Uncomment the 3 that indicate "light" or "lightweight".  Of course you must then recompile.

Third, note that this game runs fine on an Intel NUC with embedded Intel graphics, so the graphics demands are modest.

Fourth, note that adjustable OpenGL settings should favor performance.

--------------------------------------------------------------------------
Open source Ada developers are welcome to help improve or extend this game.

Please send improvements, comments, suggestions or questions to:

<fastrgv@gmail.com>

-------------------------------------------------------------------

## Open Source libraries included that allow rebuilding:
* SFML, SDL2, FLAC, ogg, vorbis, openal, glext, libz
* the included "bindings" directory contains Ada interfaces:
	* AdaPngLib
	* gl
	* sdlada

## Rebuild Requirements:
* systems:  Windows, OSX or GNU/Linux
* a recent GNAT-GPL Ada compiler from AdaLibre
* Xcode g++ compiler, if using OSX

Note that the module that defines the Ada interface to SFML-AUDIO, snd4ada_hpp.ads, was created with the command: "g++ -c -fdump-ada-spec -C snd4ada.hpp" which references a minimalistic C++ utility snd4ada.  Thus, if you redefine the interface snd4ada.hpp, you will need to recreate the interface spec snd4ada_hpp.ads by this method.




## Build instructions for AdaGate:

Three [pre-compiled] binary executables are delivered, one for Windows, one for gnu/linux and one for OSX.  I think the Windows executable is fairly portable.  It was built on Windows 10 in 32-bit mode.  The Mac binary should run on most any standard Mac with a recent version of OSX.  The linux binary, adagate_gnu, is intended to run in the presence of the directory "./libs/gnu", which contains some dynamically loaded libraries that can be, but need not be present on a target system:  SDL2, SFML, FLAC, ogg, vorbis, crypto, openal.

The distributed linux executable requires glibc v2.14 or newer.  That means if your distribution is older than june 2011, it may not run, and you will need to recompile.

Build scripts for GNAT-GPL 2015 or newer are provided;  and due to a recent script change, a Windows or linux build machine need not have a C++ compiler installed.  Only GNAT-GPL from AdaLibre is required (GNAT has its own g++).

-------------------------------------------------------
**msWin32** => wcmp32a.bat, wcmp32b.bat

**msWin64** => wcmp64a.bat, wcmp64b.bat

Note that the above windows built scripts might need to be adjusted to reference your actual installation directory for 32bit AdaCore 2017 or 64bit AdaCore 2018 compilers.


-------------------------------------------------------
**MacOSX** => ocmps.sh

build script for generating a portable executable that will run on most OSX platforms whether or not they have non-standard libraries SDL2 or SFML installed.  This is used to build the executable named adagate_osx.  Macs with a recent but standard configuration of OSX should be able to rebuild using this script, assuming you have GNAT GPL installed, as well as g++ from Xcode.

------------------------------------------------------
**GNU/Linux** => lcmpd.sh

utilizes the non-standard static libraries SDL2 & SFML, as well as other more common shared libraries that are delivered in this bundle under ./libs/gnu/.  This is used to build the [gnu/linux] executable, which should run in the presence of ./libs/gnu/, whether or not your system has those shared libraries installed.

If the delivered linux binary does not run, try...

* Manually install GNAT GPL from libre.adacore.com/download/.
* Rerun the compile script lcmpd.sh.

### Fixable Linux Link Problems:

On a linux build machine, you might get fixable link errors, depending on its configuration.  If you are missing "libz", you can simply copy "libz.so" from /usr/gnat/lib/gps/ into /usr/local/lib/.  If "libGL" cannot be found, this literally means "libGL.so" was absent.  But you might have "libGL.so.1" present.  In this case, simply create a softlink by changing to the libGL directory, then type the line:

sudo ln -s libGL.so.1 libGL.so  (and enter the admin password)

whence the linker should now be able to find what it wants.  But if there is more than one file libGL.so present on your system, make sure you use the best one;  i.e. the one that represents your accelerated-graphic-driver.


---------------------------------------------------------
**GPR note:**
There is an alternative build system included for those who prefer, and know how to use GPR:  under ./buildScriptsGpr/ .  There are 3 high level shell scripts to drive each:  gnugpr.sh, osxgpr.sh, wingpr.bat.  (They must all be moved up 1 directory to work.)



----------------------------------------------------------------------
## For Developers Only:  Portable Avatar Using Shaders

* This approach encapsulates the details of avatar shape, color, and movement within GLSL shaders and a related code object that defines vertices and texture maps.  The object may be an Ada package or C++ class.

* Programmatic inputs include uniforms for time, position, attitude, & type of motion.  The shaders then offload the realtime computational burdens onto the graphics processor.

* Data that defines shape and color, as well as the uniforms and functions that define behavior, reside completely within the object and shaders.  This data can ultimately be as detailed and refined as your imagination permits.  And any refinements made are not obfuscated in some esoteric or proprietary format with a limited audience, but remain fully portable and easily enhanced by most any developer using Free Open Source languages, tools and compilers.

* One approach would be to completely define the avatar within the shaders alone, possibly without using any texture files.  Just look at the creatures in (glslsandbox.com).  This would require advanced GLSL skills.

* But a huge selection of available MineCraft skins lead to the present avatar object design.

* In this example, the texture object is a cube with radius one that is defined as 6 disjoint cubelets.  The 2 upper quarters map to the head and torso.  The lower half is divided into 4 cubelets that are mapped to arms and legs.  The Minecraft images used for the texture also have 6 parts that map to the limbs, head and torso.

* The result is an utterly portable avatar defined by an image and 4 text files:
	* texture object body, avatarobj.adb
	* texture object spec, avatarobj.ads
	* vertex shader, avatarobj.vs
	* fragment shader, avatarobj.fs
	* any MineCraft Skin png file

* Interfacing game code with such an avatar is simple.  Essentially you need only pass the current uniform values prior to drawing.

* Of course one still needs a decent camera positioning and pointing policy within the game code in order to fully appreciate and exhibit the avatar.  The details are beyond the scope of this brief introduction, but generally the current policy is a damped and delayed move toward some fixed ideal camera position above and behind the avatar.




----------------------------------------------------------------
----------------------------------------------------------------


## what is special about this project?

For developers, this project can serve as a testbed for learning modern OpenGL and GLSL.

It uses the Ada programming language and modern OpenGL methods, with textures, shaders and uniforms.  Compiles and runs on Windows, GNU/Linux and Mac OSX systems.

Focusing on portability, transparency, and open source freedom, this project relies exclusively on F.O.S.S. tools:  a thin SDL2 binding, a thin OpenGL binding, a PNG reader by Stephen Sanguine & Dimitry Anisimkov, SFML-Audio with a homebrew binding, and a GNAT compiler.

This is one of the most functionally advanced demonstrations of "modern" OpenGL using Ada to be published as a complete F.O.S.S. application.  The term "functionally advanced" means that the code is focused on comprehensibility and completeness rather than elegance.  Further development of structure and style is left as an exercise for the coding student.

The Ada bindings are thin, so the relationship to C++ methodology is transparent.  Developers should note that these Ada bindings can be used for any OpenGL Ada project.

For the C++ programmer the code should be easy to comprehend; and for the experienced Ada programmer there are many improvements to be made to better utilize the advanced protections and features of the Ada language.  

This is a work in progress, so please excuse any scaffolding and debugging code has not been removed.

If you make improvements, please send then to <fastrgv@gmail.com>


## explanatory note on SFML versus SDL2 
Using SFML rather than SDL2 for windows and event loop management was tried, but, except for audio, SFML does NOT currently allow the core and forward compatible settings that are required to use OpenGL v3.3 on OSX.  This article:
[link](http://www.glfw.org/faq.html#how-do-i-create-an-opengl-30-context)
explains that OSX only supports forward-compatible, core profiles.  Moreover, SFML [fttb] still uses some OGL-deprecated functions (which preclude forward-compatibility).  On the other hand SDL2 audio was not used because SFML audio seemed far more elegant.  




--------------------------
## Legal Mumbo Jumbo:


AdaGate itself is covered by the GNU GPL v3 as indicated in the sources:


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
Using "sox", most sounds have recently been converted to the [non-proprietary and compact] OGG format.  Most sounds are from freesound.org and are covered by the Creative Commons Attribution noncommercial license documented in the accompanying file ccnc3_license.txt.  see also:  (http://creativecommons.org/licenses/by-nc/3.0/legalcode/)

"Among the Falls" [music for level 1], and others, are from (http://www.freesfx.co.uk).  See the file freeSFX_license.txt.

OpiumLoop is from "PartnersInRhyme": see signed authorization in ~/data/.


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


**ver 6.5.2 -- 26nov19**

* Repaired a library problem with GNU/Linux build that limited portability.
* Cleaned up several translucent png files.


**ver 6.5.1 -- 24nov19**

* Now using lightweight shaders that allow HighDpi on Mac/OSX.
* New shaders also allow smooth running on an Intel NUC, with minimal graphics capability.
* Using new, awesome lava shader & improved wormhole shader.


**ver 6.5.0 -- 22nov19**

* Updated/improved sounds & fragshaders in dungeons & wormhole.
* Reduced graphical overburden that made level 3 unplayable on older hardware.



**ver 6.4.9 -- 19nov19**

* Updated to use SDL2 v2.0.9;
* Updated Ada binding to SDL2;
* Fixed a broken level 5.



**ver 6.4.8 -- 15jun19**

* Revised monkey motion is smarter and more realistic;  limited chatter.
* Approach closer to stargates prior to wormhole effect.
* Improved code organization by moving ada source code into subdirectories: src, adabindings, adautils.
* Improved local wormhole passage.
* Generalized avatar package to draw hats, turbans.  Now default to Indiana Jones.


**ver 6.4.7 -- 24jan19**

* Improved ocean waves & foam;
* Replaced tricky & obscure frag.shader-defined lava pool with a more comprehensible implementation using coherent noise, similar to the fireball;
* Improved Stargate effects using an alternate spherical gridding & 3D Perlin coherent noise;



