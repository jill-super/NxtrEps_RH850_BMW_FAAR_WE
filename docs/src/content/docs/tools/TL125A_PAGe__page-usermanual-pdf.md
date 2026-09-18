---
title: 'TL125A_PAGe — PAGe_UserManual'
description: 'Converted PDF document PAGe_UserManual.pdf from module TL125A_PAGe.'
sidebar:
  hidden: true
---

> **Source:** `PAGe_UserManual.pdf` (PDF, 296 KB, in-module path `doc/`)
>
> Converted from PDF with text extraction; layout, vector diagrams and scanned figures are not preserved. See the source PDF in the repository for the authoritative content.
>
> pages: 23; title: -; author: -

## Converted content

### Page 1

User Guide PAGe
Project BMW AUTOSAR Core 4 Rel. 3 and adaptive BMW AUTOSAR Core Rel. 1
Author BMW AG
Release Date 2017-11-09
Version 1.1.0
Status Release
Hotline +49 89 382 - 32233 (classic) / +49 89 382 - 22522 (adaptive)
Contact bac@bmw.de (classic) / abac@bmw.de (adaptive)
https://asc.bmw.com/jira/browse/BSUP (extern)
https://asc.bmwgroup.net/jira/browse/BSUP (intern)
Company
Bayerische
Motoren Werke
Aktiengesellschaft
Postal address
BMW AG
80788 München
Office address
Forschungs- und
Innovationszentrum
(FIZ)
Hufelandstr. 1
80937 München
Telephone
Switchboard
+49 89 382-0
Internet
www.bmwgroup.com
Revision History
Version Date Changed by Description
1.1.0 2017-11-09 JC-42 Initial Documentation Release
UserGuide_PAGe, Version 1.1.0, Software Platforms Page 1 of 22

### Page 2

Table of Contents
1 Overview 3
1.1 Purpose 3
1.2 Usage 3
1.2.1 Generation 3
1.2.2 Validation 3
1.2.3 verb 3
2 Acronyms and Abbreviations 4
3 Functionality 5
3.1 Command Line Usage 5
3.2 Fileformat 5
3.3 Available Function and Objects 6
3.4 Handling of paramconf 7
3.5 Notes ARXML shortcuts 7
3.6 Loops 7
4 Examples 8
4.1 Basic Navigation 8
4.1.1 ARXML Files 8
4.1.1.1 input.arxml 8
4.1.2 pgen Files 9
4.1.2.1 input.pgen 9
4.1.3 Command line 10
4.1.4 Console Output 10
4.1.5 File Output 10
4.2 Logging 11
4.2.1 pgen Files 11
4.2.1.1 input.pgen 11
4.2.2 Command line 11
4.2.3 Console Output 11
4.2.4 File Output 11
4.3 Usage of Code Blocks 11
4.3.1 pgen Files 12
4.3.1.1 input.pgen 12
4.3.2 Command line 12
4.3.3 Console Output 12
4.3.4 File Output 12
4.4 Conditionals 13
4.4.1 ARXML Files 13
4.4.1.1 input.arxml 13
4.4.2 pgen Files 14
4.4.2.1 input.pgen 14
4.4.3 Command line 14
4.4.4 Console Output 15
4.4.5 File Output 15
4.5 More Functions 15
UserGuide_PAGe, Version 1.1.0, Software Platforms Page 2 of 22

### Page 3

4.5.1 ARXML Files 15
4.5.1.1 input.arxml 15
4.5.2 pgen Files 17
4.5.2.1 input.pgen 17
4.5.3 Command line 17
4.5.4 Console Output 17
4.5.5 File Output 17
4.6 ARXML Stuff 17
4.6.1 ARXML Files 18
4.6.1.1 input.arxml 18
4.6.2 pgen Files 19
4.6.2.1 input.pgen 19
4.6.3 Command line 19
4.6.4 Console Output 19
4.6.5 File Output 20
4.7 Filtering Elements 20
4.7.1 ARXML Files 20
4.7.1.1 input.arxml 20
4.7.2 pgen Files 21
4.7.2.1 input.pgen 21
4.7.3 Command line 21
4.7.4 Console Output 21
4.7.5 File Output 22
UserGuide_PAGe, Version 1.1.0, Software Platforms Page 3 of 22

### Page 4

1 Overview
Purpose
This user guide describes the functionality and usage of the Python AUTOSAR Generator (PAGe).
PAGe is a generator for text templates which has some knowledge of the AUTOSAR Meta Model
regarding parameter configuration. It allows easy access of modules, containers and values as well as
providing loops and verify a paramconf against a paramdef. These options are also available for postbuild.
PAGe is based on Python 3. It uses only modules of the standard library.
PAGe is designed for the usage with the BMW AUTOSAR Core modules.
Input files must have the ending .pgen which is removed from the output filename.
Usage
Generation
To generate a pgen file.
python3 -m page example.pgen
If arxmls should be used pass them to the commandline as well.
python3 -m page -o /tmp example.pgen input.arxml
Also multiple pgen files and arxml files work.
python3 -m page -o /tmp example1.pgen example2.pgen input.arxml input_new.arxml
Validation
In case you want to check a paramconf against its corresponding paramdef you can use the following
commandline python3 -m page paramconf.arxml paramdef.arxml
The validation will be performed for all the variants if an ecuc configuration is provided, too.
python3 -m page paramconf.arxml paramdef.arxml ecuc.arxml
verb
To enable a more verbose output add -v to -vvvv to the command line.
UserGuide_PAGe, Version 1.1.0, Software Platforms Page 4 of 22

### Page 5

2 Acronyms and Abbreviations
API Application Programming Interface
Application Application stands for the high-level part of software that uses the APIs
provided by the modules. It can also mean the driving application that does
not belong to the Bootloader.
AUTOSAR Automotive Open System Architecture
OS Operating System
PAGe Python AUTOSAR Generator
pgen Page generation file
UserGuide_PAGe, Version 1.1.0, Software Platforms Page 5 of 22

### Page 6

3 Functionality
PAGe builds a model of the provided ARXML paramconf and paramdefs. Within the pgen files you have
access to this model and can navigate and retrieve values easily. Besides the access to the data you have
the full power of python.
Command Line Usage
Either you install page or you add the main directory to the source path. Installation can be achieved by
python3 setup.py install
after that the page command will be available. So you can call PAGe using:
page input.pgen test.arxml -vvvv
But you may want to do install page only in a virtualenv so it does not harm any other installation.
-o Specify the output directory, default is the current directory.
--stdout do not write files, print output to stdout instead.
-vvv change level of verbosity.
-l Location to write the logfile to. Default is stdout.
-m Specify delimiter to be used in pgen files. This allows you to specify other delimiters than the default
e.g. you have files, where the defaults have a special meaning and you don’t like to escape the every
time used.
-d Enable debug mode (trap functions become active)
-V Verifies given paramconf against the paramdefs which ara supplied.
-i Add paths for the search of includes.
-D Pass variables to the pgen files ( params dictionary)
-O Change the optimisedb. This database stores the hash and the filename, so file with no change will
not be overwritten.
-f Forces write of files, even if no output change has been detected.
Fileformat
The pgen files shall be utf-8 encoded files. The files shall use unix file endings, windows file endings \r\n
are transformed to \n.
A file consists of text and several blocks that are interpreted by PAGe. These blocks are enclosed by a
special sequence of characters. %{ marks the beginning of a block and }% marks the end. The first


### Page 7

of multiple lines. For indentiation the first line is taken for reference, the rest of the indentiation has
to follow Pythons rules.
: For conditions the colon is used as a marker. It occurs at least two times, one for the condition and one
time (without extra text) for the closure. This is needed for the correct handling. You still have to use
if, elif and else keywords.
? For quick conditionals you can use a question mark. It works also directly as output. The condition
followed by a colon which seperates it from the part which is written in case of success. And an
optional second colon to seperate the ouput in the case the condition is not fullfilled.
@ This one loops over a statement. You can loop over a number of container instances, or any other
python iterateable. To iterate over a python iterateable use the syntax myitem in mycontainer which
makes the current item available as myitem. For loop over arxml elements, please have a look at ??
+ Use the plus sign for including other pgen or python files. These files are included and interpreted at
the current point within the file which they are included. A file can be included several times. Pure
python files can be included, too. By default the current path of the currently leaded source files (or
included files) is used as search directory. You can add directories using the command line switch -i
 This mark is for special handling of post build variation. It loops over the configured pre defined variants
that are configured for the ecu. Within the context of this mark, you have two special variables
available: predefined_variant_name which is the name of the current variant or None if no
variantation is configured. And predefined_variant_postfix which contains an underscore
followed by the variant name or an empt

### Page 8

set_debug Enable pdb debugging.
shortname Get the shortname at the given shortname path expressio

*Excerpt: first 8 of 23 pages shown.*
