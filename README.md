[![Build Status](https://travis-ci.org/gheja/gbdk.svg?branch=master)](https://travis-ci.org/gheja/gbdk)

GBDK
====

"The GameBoy Developer's Kit (GBDK), is a set of tools that enable to
develop programs for the Nintendo GameBoy system, either in C or in
assembly. GBDK includes a set of libraries for the most common
requirements and generates image files for use with a real GameBoy or
with an emulator like VGB or no$gmb. [...]

GBDK features:
  * An ANSI C compiler.
  * An assembler that generates relocatable code.
  * A peephole optimiser.
  * A linker that produces GameBoy image files.
  * Support for multiple-bank images.
  * Smart linking.
  * A set of libraries, with source code.
  * Example programs in assembly and in C."

From http://gbdk.sourceforge.net

Quick summary
=============

The base version (2.96a) was downloaded from the official site. Although
this is the latest version, it was released quite a while ago (back in
April 2002).

The code can be compiled in an up-to-date 64-bit Linux environment (at
least it is up-to-date here in 2016).

Original sites:
  * http://gbdk.sourceforge.net
  * http://sourceforge.net/projects/gbdk

Building
========

For the build I recommend an Ubuntu 16.04 LTS (you don't even need to
install it, the Live system works just fine).

The environment will need a few packages, all of them can be installed
using apt-get:
```
sudo apt-get -y install make gcc g++ bison flex
```

After downloading the source you can use the Makefile to compile the
binaries:
```
cd /path/where/you/extracted
make
```

Installing the compiled binaries can be done via make as well:
```
sudo make install
```

Compiling the examples:
```
cd ./gbdk-lib/examples/gb
make
```

Note: compiling the examples requires you to install the binaries you
just built in the previous steps.


Start an AWS Cloud9 instance.

Under "Platform" ensure you select "Ubuntu Server 18.04 LTS"

Load dependancies: 
```sudo apt-get -y install make gcc g++ bison flex
```

Download the repo: 
```
wget --no-check-certificate --content-disposition https://github.com/MotherTeresaHS/gbdk/archive/master.zip
```

Unzip the file: 
```
unzip gbdk-master.zip && mv gbdk-master gdbk (and rename the folder to gbdk)
```

Change director into new folder: 
```
cd gbdk
```

Run MakeFile: 
```
make
```

Then install binaries: 
```
sudo make install
```

Remove the zip file

Goto /game directory

Run: 
```
make
```

Copy game.gb over to web/rom

Open up /web/index.html
