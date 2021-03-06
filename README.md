# jpeg-9e
Stock package of jpeg9e

NOTE: This file READme.md is my personal addition to the jpeg-9e package. 
It is intended to be a quick start and pointers to the important information to get started. 
It is not intendent to replace the README file from the source package (https://github.com/intelxai/jpeg-9e/blob/main/README). 

In short, this repository contains the is the original package from the Independent 
JPEG group as found on the internet (https://www.ijg.org) as the un-tar product 
of (jpegsrc.v9e.tar.gz).

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
  coderules.txt 	Coding style rules --- please read if you contribute code.

2. Install the jpeg software package - instructions (From jpeg-9e/install.txt):

	./configure  
	make  
	make test  

If that doesn't complain, do

	make -n install

3. Where did the install process saved the resulting files?

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
  
For developers, once you have completed the installation (See steps 1. and 2. here), you can use the functionality of the package as a library. For this purpose, consult libjpeg.txt and example.c

Have fun.

Andr??


