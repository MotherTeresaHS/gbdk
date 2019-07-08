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

The version is specifically designed to run on AWS Cloud9 instance as your developement platform.

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
Run new builds of a GameBoy *.gb ROM
====================================

To build a new game, go to the ./game folder
Run the following command:
```
/opt/gbdk/bin/lcc -o game.gb game.c
```
then copy game.gb over to ./web/rom directory to see it run in simulator

Open up ./web/index.html
