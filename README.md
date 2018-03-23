![screenshot](https://github.com/fastrgv/AdaGate/blob/master/adagate.jpg)
![screenshot](https://github.com/fastrgv/AdaGate/blob/master/atollNight.jpg)


# AdaGate
AdaGate is a first-person 3D sokoban puzzle game within a Stargate / Portal fantasy setting that runs on Windows, Mac OS-X and GNU Linux.

Click on the most recent large tar.gz file under releases to download all source & binaries (both Mac & Linux), or try this link:

https://github.com/fastrgv/AdaGate/releases/download/v.6.3.1/ag23mar18.tar.gz





Video:  https://youtu.be/qgY8vF-bb8A

Video:  https://github.com/fastrgv/AdaGate/blob/master/fireball.flv


# AdaGate

## Recent Changes


**ver 6.3.1 -- 22mar18**

* Improved source code structure;  separated functions;  clarified utility names;
* Fully generalized portal geometry code to handle all 6 walls.  Now, ceiling portals in brick room, and floor portals are allowed, albeit pointless, and possibly dangerous.  Portal-hell may require using the escape-key.


**ver 6.3.0 -- 10mar18**

* Planets visible from beach are now properly initialized to correct erroneous positions;
* Improved code for texture handling;  clarified and exposed the inconsistent semantics of OpenGL textures versus cubemaps.  Now, all texture PNG images are un-inverted.


**ver 6.2.9 -- 24feb18**

* Added spinning Jupiter, Mars in beach sky.
* Improved avatarobj.ad? to support hats, etc.
* Added a link from ~/Resources/ to /data/.


## More change-history at end of file.


## AdaGate Game Description
AdaGate is a 3D sokoban puzzle game within a Stargate / Portal fantasy setting. It is a fully elaborated example of modern OpenGL programming using the Ada language that runs on Windows, OSX, and GNU/Linux.

While searching a remote south-seas atoll for remnants of a lost American heroine, a nearly operational stargate beckons.  Transported into strange dungeons, escape will require pushing every ZPM power cell onto a socket to power up the portal system. Then, blast your two portal guns at the walls to escape through the resulting wormhole.

Escape all 4 dungeons to reach the other-worldly neptune-lake, where the level of difficulty is increased for your next adventure.



## AdaGate Game Features
* Works on PCs or laptops running Windows, OSX or GNU/Linux.  And if GNAT is installed you can rebuild it yourself!  But first try the delivered binaries.
* Windows, GNU/Linux and OSX binaries provided, as well as full source. 
* Laptop friendly controls;  supports Mac Retina displays.
* A 3D Sokoban puzzle game that uses the intersection of two cylinders as a puzzle piece that rolls in two perpendicular directions.
* New stargate dial-home-device [DHD] allows non-linear play; see the island setting evolve.
* Roll the ZPMs to empower the portals and escape thru a wormhole
* Four rooms and five degrees of difficulty for a total of 20 challenging puzzles. And now solutions are available in the file ./data/solns.sok.
* Serves as a blueprint for modern OpenGL programming in Ada or C++ using GLSL 330, shaders, uniforms and textures.
* Note that Sangwine's PNG-IO library, and the Ada bindings to SFML, OpenGL & SDL2 in this app constitute a complete, yet easily extendable Ada library that could be used for most any modern OpenGL project including games, animations, simulations, modeling, or engineering.




## mouse/touchpad/keyboard controls

[You might need to disconnect unused gamecontrollers to prevent spinning!]

Look direction is controlled by touch pad or mouse;
The mouse wheel controls camera zoom.  (On a MacBook, a 2-finger swipe simulates the mouse wheel.)

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
* thumb btn: forward
* trigger btn: backward
* Ltop/Rtop btns: select/shoot
* base btn: jump

------------------------------------------------------------
### gamecontroller
* Lpaddle : attitude
* Rpaddle : movement
* Ltrigger/Rtrigger: select/shoot
* base btn: jump

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
* OSX:  must have OpenAL.framework, which comes on v10.4 and newer


### Note on Intel embedded graphics
* Such hardware use system RAM;  8Gb is enough to run but the drivers I've experienced exhibit annoying flaws, although the game is still playable.


## Setup & Running Adagate:

Windows users see also:  "windows-setup.txt"

Unzip the archive.

Windows users may see some error messages pertaining to directory links.  These links are needed only on OSX and can be ignored.

Open a commandline terminal, and cd to the install directory.

Linux users should type "adagate_gnu" to start the game.  You may also double click its icon in file manager.

Similarly, Windows users type "adagate.exe".  Note that the DLLs must be collocated with the Windows binary.

Mac users may initiate the game by navigating to the installation directory in Finder and clicking the "adagate.app" icon named "AdaGate".

The install directory should contain a subdirectory named "data".  It contains shaders, skyboxes, sound and texture data, as well as the puzzle definitions.

An optional command line parameter of 1..5 will choose the Degree-of-Difficulty [DOD], but it is normally unnecessary since the DoD increments itself after each game.  If you succeed at DoD= 3 or 4 then you are ready to try WorldCupSokerban or RufaSok!

Tips:  1) the ZPM is heavy!  If you kick it out of reach under water then you will be stranded on the island.  2) when in trouble in a dungeon, jumping may help.

By the way, you are ideally supposed to solve the sokoban puzzles without jumping back onto the walls.  On the other hand, if you jump into the puzzle at the wrong place, it might be impossible to solve.

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

Build scripts for GNAT-GPL 2015 or newer are provided;  and due to a recent script change, a linux build machine need not have a C++ compiler installed.  Only GNAT-GPL from AdaLibre is required (GNAT has its own g++).

-------------------------------------------------------
**msWin32** => wcmp.bat (assumes gnatmake.exe is "visible".

build script that requires libraries included in ./libs/win/.

-------------------------------------------------------
**MacOSX** => ocmpss.sh

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




----------------------------------------------------------------------
## For Developers Only:  Portable Avatar Using Shaders

* This approach encapsulates the details of avatar shape, color, and movement within GLSL shaders and a related code object that defines vertices and texture maps.  The object may be an Ada package or C++ class.

* Programmatic inputs include uniforms for time, position, attitude, & type of motion.  The shaders then offload the realtime computational burdens onto the graphics processor.

* Data that defines shape and color, as well as the uniforms and functions that define behavior, reside completely within the object and shaders.  This data can ultimately be as detailed and refined as your imagination permits.  And any refinements made are not obfuscated in some esoteric or proprietary format with a limited audience, but remain fully portable and easily enhanced by most any developer using Free Open Source tools and compilers.

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

* Of course one still needs a decent camera positioning and pointing policy within the game code in order to fully appreciate and exhibit the avatar.




----------------------------------------------------------------
----------------------------------------------------------------


## what is special about this project?

For developers, this project can serve as a testbed for learning modern OpenGL and GLSL.

Uses the Ada programming language and modern OpenGL methods, with textures, shaders and uniforms.  Compiles and runs on Windows, GNU/Linux and Mac OSX systems.

Focusing on portability, transparency, and open source freedom, this project relies exclusively on F.O.S.S. tools:  a thin SDL2 binding from Dan Vazquez (modified), a thin OpenGL binding from "Lumen", a PNG reader by Stephen Sanguine, SFML-Audio with a homebrew binding, and a GNAT compiler.

This is one of the most functionally advanced demonstrations of "modern" OpenGL using Ada to be published as a complete F.O.S.S. application.  By "functionally advanced", it is meant that the code is focused on comprehensibility and completeness rather than elegance.  Further development of structure and style is left as an exercise for the coding student.

The Ada bindings are thin, so the relationship to C++ methodology is transparent.  Developers should note that these Ada bindings can be used for any OpenGL Ada project.

For the C++ programmer the code should be easy to comprehend; and for the experienced Ada programmer there are many obvious improvements to be made.  

This is a work in progress, so please excuse scaffolding and debugging code has not been removed.

If you make improvements, please send then to <fastrgv@gmail.com>


## explanatory note on SFML versus SDL2 
Using SFML rather than SDL2 for windows and event loop management was tried, but, except for audio, SFML does NOT currently allow the core and forward compatible settings that are required to use OpenGL v3.3 on OSX.  This article:
[link](http://www.glfw.org/faq.html#how-do-i-create-an-opengl-30-context)
explains that OSX only supports forward-compatible, core profiles.  Moreover, SFML [fttb] still uses some OGL-deprecated functions (which preclude forward-compatibility).  On the other hand SDL2 audio was not used because SFML audio seemed far more elegant.  




--------------------------
## Legal Mumbo Jumbo:


AdaGate itself is covered by the GNU GPL v3 as indicated in the sources:


 Copyright (C) 2017  <fastrgv@gmail.com>

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

My first choice for epilog music was Tim Larkin's Kadish-Gallery music from Uru, but as AdaGate is F.O.S.S. I could not redistribute that.  But I can still suggest using it, if you know how and can find it on you-tube.

### ImageFiles 
Most images for textures were freely [no copyright indications] available on google images.  Some wall textures used are from the GPL2.0/GPL3.0-only section of OpenGameArt.Org.  One other thatched roof texture was used from http://www.mayang.com/textures.  See mayang_license.txt.  Others from pixabay.com have a CC0 license.  More recently, some are from http://all-free-download.com/free-photos/.

### ShaderFiles 
Several fragment shader files used were downloaded from http://glslsandbox.com/ and put under ./data/.  All frag. shaders from glslsandbox are under the MIT license (see mit_license.txt).  Existing comments or any identifying information was retained.  What follows are acknowledgments for those that were identifyable.

"Red Planet" from Mahmud Yuldashev <mahmud9935@gmail.com>, and "waterWorldCCNSA3.fs" with a CreativeCommons license, and which seems to be credited to Alexander Alekseev with mods by Mahmud Yuldashev.

In order to make any of these usable, I had to modernize them to glsl version 330 specifications, and adapt them to utilize some additional uniforms for input.

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

**ver 6.2.8 -- 28jan18**

* Corrections to restore proper function in 1st person.
* Sokoban view improvements.
* Enhanced playability.


**ver 6.2.7 -- 25jan18**

* Further improvements in camera system and playability.


**ver 6.2.6 -- 22jan18**

* Improvement of the virtual camera system, which remains a relatively smart "tracking" type.  It now allows better views of the sokoban puzzle areas and the stargate Dial-Home-Device.  It has better backward movement and reduced jitter.
* Added mousewheel adjustability of camera zoom.
* Corrected third-person optics in ocean.
* Improved island movement over sand hills and around trees & rocks.
* Corrected vertical angle for third-person shooting within portal.



**ver 6.2.5 -- 16jan18**

* improved avatar control;
* much improved camera handling;
* corrected geometry for third-person shooting within portal;


**ver 6.2.4 -- 11jan18**

* improved dungeon fog shader coding and realism.
* improved green mamba, lava turtle & avatar;
* improved lighting in magma room; magma ball now emits diffuse light;


**ver 6.2.3 -- 19dec17**

* Updated to SDL v2.0.7 on Linux, Windows.
* Updated to SDL v2.0.7x on OSX.
* Added low hanging FOG to 2 of 5 beach prologs:
	a)skyboxes; b)ocean; c)trees; d)sand; e)rocks.


**ver 6.2.2 -- 18nov17**

* Reverted back to SDL v2.0.3 due to problems with newer version.

**ver 6.2.1 -- 17nov17**

* Created new minimal Ada binding for SDL v2.0.7;
* Updated scripts, libs to use SDL v2.0.7;
* Modified & simplified ocean shaders to repair a fissure in the sea, that only appeared on certain hardware.
* Fixed shooting thru portals when avatar is showing.
* Made several adjustments to reduce jitter on modest graphical hardware and on Macs running HiDpi:
	* Reduced ocean's grid resolution;
	* Reduced level2 reflective pool grid;
	* Changed level4 dark pool fragshader.


**ver 6.2.0 -- 11nov17**

* Added prebuilt executables for msWindows !!
* Added working build scripts for msWindows !!
* Corrected wrong linux SDL libraries in previous release!

* Updated OSX to use SFML v2.4.2;
* Added startup messages giving OGL version/profile;
* Improved compile scripts;  removed unused libraries;


**ver 6.1.4 -- 29jun17**

* Updated linux scripts to use a) SFML v2.4.2;  b) AdaCore 2017;
* Note that AdaCore 2017 works on OSX with no changes.
* Implemented a conformal texture map for rocks, coconuts;
* Improved ocean opacity using a simplified Fresnel effect.


**ver 6.1.3 -- 15apr17**

* Improved avatar movement in water;  added treadwater motion;
* Corrected errors in portal drawing geometry when in third person mode;


**ver 6.1.2 -- 31mar17** (0)

* Simplified the portal discard technique used to draw only what is within each portal's field of view.
* Added avatar that can use most any minecraft skin.  Current one is set to DukeNukem or PrincessJasmine.  Others included under ./data/avatars/.  Simple copy desired image to "./data/skin.png".  To toggle 3rd person, use (m)-key.


**ver 6.1.1 -- 12mar17** (12)

* Added an awesome rolling fireball in the brick dungeon.  Shaders project vertices from a cubical shell onto a spherical shell to avoid singularities.  Then a coherent 3D noise function is used to define perturbations whose magnitudes index into a 1D colormap with black, red, orange, yellow, and white.


**ver 6.1.0 -- 3mar17**

* Removed OpenGL-deprecated functions and enums that may have caused aborts.
* Improved GL error handling.


**ver 6.0.9 -- 7feb17**

* Improved reflective water motion, magma pool motion & color;  added window frames.
* Added magma-glow effects.  This required new utilities, new objects with defined normals, and new shaders.
* Fixed bad multi colored fish texture.
* Improved the coding and readability of several object packages.
* Added lava turtle to help prepare for my next project (guesses?).


**ver 6.0.8 -- 5jan17**

* Corrected a duplicate window glitch.
* Refined compiler scripts.


**ver 6.0.7 -- 29dec16**

* Added WASD keys for movement.
* Improved build system to be compatible with more linux distros.
* Improved OpenGL coding to run on less capable graphics hardware.


**ver 6.0.6 -- 30nov16**

* Improved linux build scripts.  Omitted one failed OSX script.
* Now uses an improved interface binding Ada to SFML audio.
* Now using SFML 2.4.1.
* Replaced the most graphically-demanding fragment shader in order to allow AdaGate to run on cheaper Intel embedded graphics chips, such as might be found on economical laptops and mini-desktop computers.
* Updated OSX bundling.


**ver 6.0.5 -- 6nov16**

* Improved handling of the case of 2 portals on the same wall by creating shaders that can discard an unwanted [overlapping] halfspace.  Such a technique might be of interest to glsl developers, but not game players.
* Improved movement within the island scenes by changing the deep water boundary action to be a tangential deflection rather than a dead stop.
* Corrected errors in defining palm tree keepouts on island.  Now, you will bump them and not pass through them.


**ver 6.0.4 -- 20oct16**

* Fixed errors that caused erroneous textures to appear when portals were open.
* Added capability to shoot at a target seen through a portal.  This augments possible strategies for escaping a dungeon to allow escape with a single teleportation.
* Remedied an apparent error when both portals are on the same wall.  In this case, their two virtual worlds overlap and interfere with each other.  FTTB, only the closer one is drawn (unless their heights are equal).
* The TARDIS makes a twisting debut.


**ver 6.0.3 -- 27sep16**

* improved oarfish appearance.
* improved the tree drawing technique to use fewer resources and simplify logic.
* corrected portal gun aimpoints when not high enough above ledges.
* revised dungeon portals to allow a see-thru view to destination rather than showing an opaque stargate texture.  This enhancement was quite complex because it required the derivation of some magical transormation equations, as well as modifying the fragment shader to create a transparent spot on an existing wall texture.


**ver 6.0.2 -- 03jul16**

* added lava shriek.
* improved snd4ada.cpp
* Added gnat project files for OSX and GNU-linux, for any developers who prefer them, as well as an unfinished prototype for MSWin.  Any volunteer developers with an MSWindows platform that might be able to finish it are welcomed to try.  (I abandoned MSWin in 1999)
* A description of the 5 legacy compilation scripts follows:
	* lcmp.sh : Linux, all shared libs
	* lcmps.sh : Linux some static libs
	* lcmpss.sh : Linux maximal static libs
	* ocmps.sh : OSX some statics
	* ocmpss.sh : OSX maximal statics


**ver 6.0.1 -- 7may16**

* Updated OpenAL frameworks and static libraries that remove deprecation warning on OSX.  These allow compilation scripts that deliver even more portable binaries for both OSX and Gnu/Linux.
* Small improvements/corrections in palm swaying motion and sounds.
* Cleaned up scripts and libraries.


**ver 6.0 -- 26apr16**

* Updated audio to use SFML version 2.3.2.  A new advantage is that OGG format sound files can be used.  These are smaller and non-proprietary.
* The OSX build system for AdaGate now uses included Frameworks for common but not universal OGG/Vorbis libraries, and static SFML libs.
* Similarly updated the gnu-linux build system to facilitate using the new SFML static libraries and included shared libs for OGG/Vorbis.


**ver 5.9.1 -- 12apr16**

* Fixed critical error within ./libs/gnu/ that prevented the GNU-Linux executable from being able to find necessary shared libraries.  Several additional softlinks solved this problem.


**ver 5.9.0 -- 8apr16**

* Reverted to SFML v2.1 for portability and build simplicity.
* Improved directory structure;
* Reduced size of largest WAV files by trimming to 30 seconds;
* Higher percent static libs used in gnu/linux compile script;
* All nonstandard libraries are static in OSX compile script.


**ver 5.7 and 5.8**
* attempted using newer SFML library...but reverted.

**ver 5.6 -- 22mar16**

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
* added an **optional**, user-edittable text file (settings.txt) to adjust gamepad/joystick settings.  This means you can now adjust sensitivity and remap the buttons using a text editor.  Note that there is a strict format, if present.


**ver 5.0 -- 31dec15**

* removed splashing sound in prolog because it was problematic.  It prevented game controllers from working on OSX.
* disabled HDPI mode on the delivered OSX binary.  Now AdaGate runs noticably smoother (with no jitter) and looks better.  Of course, you may enable it before you rebuild, if desired.
* joysticks and gamecontrollers can now be used (without needing any special drivers in linux or OSX) for AdaGate:
	* joystick contols attitude; thumb button moves forward;  trigger button moves backward;  topleft or topright buttons select on DHD and shoot portal guns;  nearest base button initiates a jump.
	* gamecontroller:  left paddle controls attitude;  right paddle controls movement;  left or right trigger buttons select on DHD and shoot portal guns;  nearest base button initiates a jump.



