# jpeg-9e
Stock package of jpeg9e

NOTE: This file README.md is my personal addition to the jpeg-9e package. 
It is intended to be a quick start and pointers to the important information to get started. 
It is not intendent to replace the README file from the source package (https://github.com/intelxai/jpeg-9e/blob/main/README). 

In short, this repository contains the is the original package from the Independent 
JPEG group as found on the internet (https://www.ijg.org) as the un-tar product 
of (jpegsrc.v9e.tar.gz).

For background information on libjpeg you may want to see https://en.wikipedia.org/wiki/Libjpeg

0. Clone this git repository

	% git clone git@github.com:intelxai/EXT_libjpeg-9e

1. If it is your first time with jpeg check the following documentation files:

User documentation (From the jpeg-9e/README file):

	install.txt		How to configure and install the IJG software.
	usage.txt 		Usage instructions for cjpeg, djpeg, jpegtran and more
	*.1			Unix-style man pages for programs (same info as usage.txt).
	wizard.txt		Advanced usage instructions for JPEG wizards only.
	cdaltui.txt		Description of alternate user interface for cjpeg/djpeg.
	change.log		Version-to-version change highlights.

Programmer and internal documentation:

	libjpeg.txt		How to use the JPEG library in your own programs.
	example.c		Sample code for calling the JPEG library.
	structure.txt		Overview of the JPEG library's internal structure.
	filelist.txt		Road map of IJG files.
	coderules.txt		Coding style rules --- please read if you contribute code.

2. Install the jpeg software package - instructions (From jpeg-9e/install.txt):

	./configure  
	make  
	make test  
	
NOTE: Unlike many libraries, the main api include file "jconfig.h" is not included in the 
package as a file. Instead, the ./configure script above will produce it. If you run into 
troubles the first place to look is in config.log. See  jconfig.txt from this repository 
for explanations

If the instructions at step (2.) doesn't produce errors, do

	make -n install

3. Where did make saved the resulting files?

On my unix systems (MacOS and Linux) the following where produced as executable binairies

	/usr/local/bin/cjpeg  
	/usr/local/bin/djpeg   
	/usr/local/bin/jpegtran   
	/usr/local/bin/rdjpgcom   
	/usr/local/bin/wrjpgcom   

And the following where produced as linkable libraries

	/usr/local/lib/libjpeg.a   
	/usr/local/lib/libjpeg.la   
	/usr/local/lib/libjpeg.so   
	/usr/local/lib/libjpeg.dylib -> libjpeg.9.dylib   
	/usr/local/lib/libjpeg.la   
	/usr/local/lib/pkgconfig  (A directory)   

NOTE: On my linux systems I needed to run step 2. as superuser for the files to be copied 
at these locations. 

4. Use the utilities (From jpeg-9e/usage.txt)

Two most generaly usefull programs are: cjpeg to compress an image file into JPEG format,
and djpeg to decompress a JPEG file back into a conventional image format.

On Unix-like systems, you invoke:

	cjpeg [switches] [imagefile] >jpegfile
or
	djpeg [switches] [jpegfile]  >imagefile

On most non-Unix systems, you say:

	cjpeg [switches] imagefile jpegfile
or
	djpeg [switches] jpegfile  imagefile

For more usage 

	cjpeg -help
	
and

	djpeg -help


Have fun.

André


