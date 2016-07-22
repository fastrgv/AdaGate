![screenshot](https://github.com/fastrgv/AdaGate/blob/master/atollNight.jpg)

# AdaGate
AdaGate is a first-person 3D sokoban puzzle game within a Stargate / Portal fantasy setting that runs on Mac OS-X and GNU Linux.

Click on the large tar.gz file under releases to download all source & binaries (both Mac & Linux)

or Click on [raw] "adagate-src-only-snapshot.tar.gz" to download source only.


# AdaGate -- v 6.0.2

## Whats new:

**ver 6.0.2 -- 03jul16**

* added lava shriek.
* improved snd4ada.cpp
* Added gnat project files for OSX and GNU-linux, for any developers who prefer them, as well as an unfinished and untested prototype for MSWin.  Any volunteer developers with an MSWindows platform that might be able to finish it are welcomed to try.  (I abandoned MSWin in 1999)
* A description of the 6 legacy compilation scripts follows:
	* lcmp.sh : Linux, all shared libs
	* lcmps.sh : Linux some static libs
	* lcmpss.sh : Linux maximal static libs
	* ocmp.sh : OSX minimal statics
	* ocmps.sh : OSX some statics
	* ocmpss.sh : OSX maximal statics


**ver 6.0.1 -- 7may16**

* Updated OpenAL frameworks and static libraries that remove deprecation warning on OS-X.  These allow compilation scripts that deliver even more portable binaries for both OS-X and Gnu/Linux.
* Small improvements/corrections in palm swaying motion and sounds.
* Cleaned up scripts and libraries.

**ver 6.0 -- 26apr16**

* Updated audio to use SFML version 2.3.2.  A new advantage is that OGG format sound files can be used.  These are smaller and non-proprietary.
* The OS-X build system for AdaGate now uses included Frameworks for common but not universal OGG/Vorbis libraries, and static SFML libs.
* Similarly updated the gnu-linux build system to facilitate using the new SFML static libraries and included shared libs for OGG/Vorbis.


**ver 5.9.1 -- 12apr16**

* Fixed critical error within ./gnulibs/ that prevented the GNU-Linux executable from being able to find necessary shared libraries.  Several additional softlinks solved this problem.


**ver 5.9.0 -- 8apr16**

* Reverted to SFML v2.1 for portability and build simplicity.
* Improved directory structure;
* Reduced size of largest WAV files by trimming to 30 seconds;
* Higher percent static libs used in gnu/linux compile script;
* All nonstandard libraries are static in OS-X compile script.


**ver 5.7 and 5.8**
* attempted using newer SFML library...but reverting.

**ver 5.6 -- 22mar16 (last delivery with SFML v2.1)**

* Fixed several minor problems;  improved various other settings, sounds.
* Using awesome new swiss-cheese wormhole shader.
* Exposed curious jar buried in sand.

**ver 5.5 -- 13mar16**

* Improved ocean shader, finer angular gridding;  noticeably more realistic opacity when looking thru surf toward deeper ocean, yet fish are still visible.
* Darkened nightime trees & sand for improved realism.

**ver 5.4 -- 5mar16**

* added more wormhole effects, some with a heavier graphical burden, one for dungeon-local travel, and one for return to island.
* wormhole effects are now extended to all teleportation except flyover at initial startup.
* fixed high wormhole exit physics-error of not dropping to ground level.

**ver 5.3 -- 29feb16**

* added an awesome new spinning and disorienting wormhole cutscene effect whenever passing through a stargate.
* fixed other minor problems.


**ver 5.21 -- 26feb16**

* fixed an error that caused portal gun problems;
* improved serpent texture.


**ver 5.2 -- 19feb16**

* enhanced fish-shader to allow contrary rotations.
* created contrary green mamba with articulated round body.
* A new Mac-Binary-Bundle that acts like a normal Mac App is now delivered.  This app is delivered in the installation directory, but could be moved elsewhere, such as your personal Applications directory [and initiated with a click].  Note that there are some soft [symbolic] links in the bundle that are resolved automatically when copied with the command "cp -r adagate.app destination-directory".


**ver 5.1 -- 04jan16**

* got prolog splash sound to work using sfml:sound, rather than sfml:music.
* added an optional, user-edittable text file (settings.txt) to adjust gamepad/joystick settings.  This means you can now adjust sensitivity and remap the buttons using a text editor.  Note that there is a strict format, if present.


**ver 5.0 -- 31dec15**

* removed splashing sound in prolog because it was problematic.  It prevented game controllers from working on OS-X.
* disabled HDPI mode on the delivered OS-X binary.  Now AdaGate runs noticably smoother (with no jitter) and looks better.  Of course, you may enable it before you rebuild, if desired.
* joysticks and gamecontrollers can now be used (without needing any special drivers in linux or OS-X) for AdaGate:
	* joystick contols attitude; thumb button moves forward;  trigger button moves backward;  topleft or topright buttons select on DHD and shoot portal guns;  nearest base button initiates a jump.
	* gamecontroller:  left paddle controls attitude;  right paddle controls movement;  left or right trigger buttons select on DHD and shoot portal guns;  nearest base button initiates a jump.






## what is special about this project?
Uses the Ada programming language and fully modern OpenGL methods, with textures, shaders and uniforms.  Achieves version 3.3 core profile contexts.  Compiles and runs on both GNU/Linux and Mac OS-X systems.  This project serves as a testbed for learning the complexities of modern OpenGL and GLSL.

Focusing on portability and freedom, no coding effort or compromise has been made to accomodate proprietary operating systems.  It relies on free open source software:  a thin SDL2 binding from Dan Vazquez, a thin OpenGL binding from "Lumen", a PNG reader by Stephen Sanguine, and SFML-Audio (because of its elegant audio interface).

If one defines "modern" OpenGL to mean version 3.3 or higher, then this may be the most functionally advanced demonstration of "modern" OpenGL using Ada to be found.  Written in C++ style, the code neglects many safety features available to Ada, but it does serve as a fully functional example that focuses on learning OpenGL.  The Ada bindings are thin, so the relationship to C++ methodology is transparent.  Developers should note that these Ada bindings can be used as a standalone library for most any OpenGL project that uses Ada.

Thus, for the C++ programmer the code should be easy to comprehend; and for the experienced Ada programmer there are many potential improvements to be made.  Suggestions are welcomed, as are coding or design improvements.  Just send to <fastrgv@gmail.com>.


## explanatory note on SFML versus SDL2 
Using SFML rather than SDL2 for windows and event loop management was tried, but SFML does NOT currently allow the core and forward compatible settings that are required to use OpenGL v3.3 on OS-X.  This article:
[link](http://www.glfw.org/faq.html#how-do-i-create-an-opengl-30-context)
explains that OSX only supports forward-compatible, core profiles.  Moreover, SFML [fttb] still uses some OGL-deprecated functions (which preclude forward-compatibility).  On the other hand SDL2 audio was not used because SFML audio seemed far more elegant.  


## AdaGate Game Description
AdaGate is a first-person 3D sokoban puzzle game within a Stargate / Portal fantasy setting. It is a great example of modern OpenGL programming using the Ada language. 

While searching a remote south-seas island for remnants of a lost American heroine, an operational stargate lures you into 4 strange dungeon rooms, with no obvious exit. Escape will require the logical rearrangement of weird power cells [ZPMs] that roll in only two directions. Shoot your portal guns at the dungeon walls to configure 2 escape portals, but in order to activate them, all of the ZPMs must be bumped onto their sockets. But beware: you can only PUSH the ZPMs, so you will fail if you roll one into a corner or against a wall. But dont worry, cheating is pretty easy ; )

With 5 degrees of difficulty [DoD], there are 20 user-replaceable puzzles to solve. Escape all 4 dungeons to reach the neptune choir skybox and increment the DoD for your next challenge.



## AdaGate Game Features
* Works on PCs or laptops running OS-X or GNU/Linux.  And if GNAT is installed you can build it yourself!  But first try the delivered binaries.
* Both GNU/Linux and OS-X binaries provided, as well as full source. 
* Laptop friendly controls;  supports Mac Retina displays.
* A first-person (you are the pusher) 3D Sokoban puzzle game that uses the intersection of two cylinders as a puzzle piece that rolls in two perpendicular directions.
* New stargate dial-home-device [DHD] allows non-linear play; watch island setting evolve.
* Roll the cylindrical ZPMs to empower the portals and escape thru a wormhole
* Four rooms and five degrees of difficulty for a total of 20 challenging puzzles. And now solutions are available in the file ./data/solns.sok.
* Serves as a blueprint for modern OpenGL programming in Ada or C++ using GLSL 330 and shaders.
* Note that the Ada bindings to OpenGL & SDL2 in this app are usable as a standalone library for most any modern Ada project.
* See also: WorldCupSokerban, a 3rd-person 3D sokoban game within a soccer field. Comes with an autosolver!



## mouse/touchpad/keyboard controls

[You might need to disconnect unused gamecontrollers to prevent spinning!]

Look direction is controlled by touch pad or mouse;

Movement is controlled by the arrow keys:

		(Up)
	(Lt)	(Dn)	(Rt)

Shoot the two portal guns using:  (L)-key (R)-key, or (if you have two) the two mouse buttons.

(space)-key => jump up/over short walls

(esc)-key => exit;  

### joystick
* joystick : attitude
* thumb btn: forward
* trigger btn: backward
* Ltop/Rtop btns: select/shoot
* base btn: jump

------------------------------------------------------------
### gamecontroller
* Lpaddle : attitude
* Rpaddle : movement
* Ltrigger/Rtrigger: select,shoot
* base btn: jump

------------------------------------------------------------
### settings
If the need arises, copy the file "default_settings.txt" to "settings.txt".  Then you can manually edit the integers that define the key-bindings or the floats that define the sensitivities.

------------------------------------------------------------

If you ever get stuck, try to jump up & forward/back.

------------------------------------------------------------
------------------------------------------------------------


## required for running:

* graphics card & driver that supports OpenGL version 3.3 or later;
* GNU/Linux or a Mac running OS-X;
* optional game controller or joystick.


## Open Source libraries included for rebuilding:
* SFML, SDL2, FLAC, ogg, vorbis, freetype, jpeg, openal
* the included "bindings" directory contains Ada interfaces:
	* AdaPngLib
	* gl
	* sdlada

## Rebuild Requirements:
* systems:  OS-X or GNU/Linux
* a recent gnat compiler

Note that the module that defines the Ada interface to SFML-AUDIO, snd4ada_hpp.ads, was created with the command: "g++ -c -fdump-ada-spec -C snd4ada.hpp" which references a minimalistic C++ utility snd4ada.  Thus, if you redefine the interface snd4ada.hpp, you will need to recreate the interface spec snd4ada_hpp.ads by this method.


## Running adagate:
Unzip the archive and you will see a new directory appear with a name like "bundle_date", that you should rename to something like "adagate_install_directory".  

Linux users should then cd to adagate_install_directory, then type "adagate_gnu" to start the game.  You may also double click its icon in file manager.

Mac users may initiate the game by navigating to the installation directory in Finder and clicking the "adagate.app" icon named "AdaGate".

The adagate_install_directory should contain a subdirectory named "data".  It contains shaders, skyboxes, sound and texture data, as well as the puzzle definitions.

An optional command line parameter of 1..5 will choose the Degree-of-Difficulty [DOD], but it is normally unnecessary since the DoD increments itself after each game.  If you succeed at DoD= 3 or 4 then you are ready to try WorldCupSokerban or RufaSok!

Caution, the ZPM is heavy!  If you kick it out of reach under water then you will be stranded on the island.

By the way, you are ideally supposed to solve the sokoban puzzles without jumping back onto the walls.  If you do, it might be said that you cheated!  Conversely, if you jump into the puzzle at the wrong place, it might be impossible to solve.

--------------------------------------------------------------------------
Open source Ada developers are welcome to help improve or extend this game.

Developer or not, send comments, suggestions or questions to:

<fastrgv@gmail.com>




## Build instructions for AdaGate:

Two [pre-compiled] binary executables are delivered, one for gnu/linux and one for OS-X.  The Mac binary should run on most any standard Mac with a recent version of OS-X.  The linux binary, adagate_gnu, is intended to run in the presence of the directory "gnulibs", which contains some dynamically loaded libraries that can be, but need not be present on a target system:  SDL2, SFML, FLAC, ogg, vorbis, freetype, jpeg, openal.

Build scripts for GNAT2015 or newer are provided.  Suggestions or help improving the build process is welcome.

-------------------------------------------------------
**MacOSX** => ocmpss.sh:

build script for generating a portable executable that will run on most OS-X platforms whether or not they have non-standard libraries SDL2 or SFML installed.  This is used to build the executable named adagate_osx.  Macs with a recent but standard configuration of OS-X should be able to rebuild using this script, assuming you have GNAT GPL installed.

------------------------------------------------------
**GNU/Linux** => lcmpss.sh

utilizes the non-standard static libraries SDL2 & SFML, as well as other more common shared libraries that are delivered in this bundle under ./gnulibs/.  This is used to build the [gnu/linux] executable, which should run in the presence of ./gnulibs/, whether or not your system has those shared libraries installed.  Note that the runtime loader will prefer system libraries if they are present. 

The current build is compiled on OpenSUSE v13.2, and uses GLIBC 2.14 [dating from june 2011].  This generally means that if your linux distro uses glibc v2.14 or newer, then the prebuilt binary should probably run on your system (and be rebuildable).

If the delivered linux binary does not run...

* Manually install GNAT GPL from libre.adacore.com/download/.
* Rerun the compile script lcmp.sh or lcmps.sh or lcmpss.sh.




--------------------------
## Legal Mumbo Jumbo:


AdaGate itself is covered by the GNU GPL v3 as indicated in the sources:


 Copyright (C) 2016  <fastrgv@gmail.com>

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
The particular choices of sound, image, and fragment shader files [x.fs] delivered are not essential to the function of the game and are easily replaced.  This software is primarily intended as a tutorial example of modern OpenGL methods using GLSL.  The only requirements are that sounds be in WAV or OGG format, images be in PNG format, and shaders be updated to GLSL 330 specifications.  Skybox images have an additional constraint, they must also have a 90x90 degree field of view [for a correct perspective], and all 6 must have the same pixel dimensions.

### Defining Your Own Puzzles:
  Read puzzle_replacement.txt

### SoundFiles
Using "sox", most sounds have recently been converted to the [non-proprietary and compact] OGG format.  Most sounds are from freesound.org and are covered by the Creative Commons Attribution noncommercial license documented in the accompanying file ccnc3_license.txt.  see also:  (http://creativecommons.org/licenses/by-nc/3.0/legalcode/)

"Among the Falls" [music for level 1], and others, are from (http://www.freesfx.co.uk).  See the file freeSFX_license.txt.

My first choice for epilog music was Tim Larkin's Kadish-Gallery music from Uru, but as AdaGate is F.O.S.S. I could not redistribute that.  But I can still suggest using it, if you know how and can find it on you-tube.

### ImageFiles 
Most images for textures were freely [no copyright indications] available on google images.  Some wall textures used are from the GPL2.0/GPL3.0-only section of OpenGameArt.Org.  One other thatched roof texture was used from http://www.mayang.com/textures.  See mayang_license.txt.  Others from pixabay.com have a CC0 license.  More recently, some are from http://all-free-download.com/free-photos/.


### ShaderFiles 
Several fragment shader files used were downloaded from http://glslsandbox.com/ and put under ./data/.  All frag. shaders from glslsandbox are under the MIT license (see mit_license.txt).  Existing comments or any identifying information was retained.  What follows are acknowledgments for those that were identifyable.

"Red Planet" from Mahmud Yuldashev <mahmud9935@gmail.com>, and "waterWorldCCNSA3.fs" with a CreativeCommons license, and which seems to be credited to Alexander Alekseev with mods by Mahmud Yuldashev.

In order to make any of these usable, I had to modernize them to glsl version 330 specifications, and adapt them to utilize some programatic uniforms for input.



### SkyBoxes 
For some of these, I lowered the horizon slightly for technical reasons;  and for others I converted to png files with RGBA mode.

One source is (www.custommapmakers.org/skyboxes.php), which gathers together many free-to-use skyboxes.

Another skybox  [from  (http://www.redsorceress.com/skybox.html)]  is credited to "The Mighty Pete" at http://www.petesoasis.com (which seems defunct).

Another skybox used [from OpenGameArt.org] is the work of Heiko Irrgang <hi@93-interactive.com> and is licensed under the Creative Commons Attribution-ShareAlike 3.0 Unported License.  To view a copy of this license, visit (http://creativecommons.org/licenses/by-sa/3.0/) or send a letter to Creative Commons, 444 Castro Street, Suite 900, Mountain View, California, 94041, USA.  See also the accompanying file ccsa3_license.txt.

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

----------------------------------------------------------------

