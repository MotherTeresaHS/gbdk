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

Build
=====

Start an AWS Cloud9 instance.

Under "Platform" ensure you select "Ubuntu Server 18.04 LTS"

Load dependancies: 
```
sudo apt-get -y install make gcc g++ bison flex
```

Download the repo: 
```
wget --no-check-certificate --content-disposition https://github.com/MotherTeresaHS/gbdk/archive/master.zip
```

Unzip the file (and rename the folder to gbdk): 
```
unzip gbdk-master.zip && mv gbdk-master gbdk && rm gbdk-master.zip
```

Change director into new folder: 
```
cd gdbk
```

Run MakeFile: 
```
make
```

Then install binaries: 
```
sudo make install
```

Install this tool, to make sprite tiles from PNG files

Run: 
```
npm install -g ggbgfx-cli
```

Copy game.gb over to web/rom to see it run in simulator

Open up /web/index.html
