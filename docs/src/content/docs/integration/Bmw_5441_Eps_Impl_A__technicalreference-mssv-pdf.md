---
title: '_Bmw_5441_Eps_Impl_A — TechnicalReference_MSSV'
description: 'Converted PDF document TechnicalReference_MSSV.pdf from module _Bmw_5441_Eps_Impl_A.'
sidebar:
  hidden: true
---

> **Source:** `TechnicalReference_MSSV.pdf` (PDF, 624 KB, in-module path `doc/`)
>
> Converted from PDF with text extraction; layout, vector diagrams and scanned figures are not preserved. See the source PDF in the repository for the authoritative content.
>
> pages: 22; title: YourTopic; author: Markus Groß, Patrick Markl

## Converted content

### Page 1

MICROSAR Safe Silence Verifier 
Technical Reference 
 
 
Version 1.4 
 
 
 
 
 
 
 
 
 
 
 
Authors Markus Groß, Patrick Markl 
Status Released

### Page 2

Technical Reference MICROSAR Safe Silence Verifier 
2014, Vector Informatik GmbH Version: 1.4 
based on template version 4.11.3 
2 / 22 
Document Information 
History 
Author Date Version Remarks 
Markus Groß 2012-07-24 1.0 Initial version 
Patrick Markl 2012-08-22 1.1 Changes after review 
Markus Groß 2012-11-15 1.2 Add information about third party libraries 
Markus Groß 2013-01-15 1.3 Update to reflect changes 
Patrick Markl 2014-03-03 1.4 Added restrictions chapter 
Reference Documents 
No. Source Title Version 
[1] ISO ISO/IEC 9899:1990, Programming languages -C Second 
edition

### Page 3

Technical Reference MICROSAR Safe Silence Verifier 
2014, Vector Informatik GmbH Version: 1.4 
based on template version 4.11.3 
3 / 22 
Contents 
1 Introduction................................ ................................ ................................ ................... 6 
1.1 Intended audience ................................ ................................ ............................. 6 
2 Functional Description ................................ ................................ ................................ . 7 
2.1 Required Environment ................................ ................................ ....................... 7 
2.2 Restrictions ................................ ................................ ................................ ........ 7 
2.3 Command Line Parameters ................................ ................................ ............... 7 
2.3.1 Option -h, --help ................................ ................................ ................. 8 
2.3.2 Option --version ................................ ................................ ................. 8 
2.3.3 Option -v, --verbose ................................ ................................ ............ 8 
2.3.4 Option --crcCheck ................................ ................................ .............. 8 
2.3.5 Option --openReport ................................ ................................ .......... 8 
2.3.6 Option --stats ................................ ................................ ................ 8 
2.3.7 Option -l, --logFile ................................ ................................ .............. 8 
2.3.8 Option -r, --reportFile ................................ ................................ .......... 9 
2.3.9 Option -p, --pluginDir ......

### Page 4

Technical Reference MICROSAR Safe Silence Verifier 
2014, Vector Informatik GmbH Version: 1.4 
based on template version 4.11.3 
4 / 22 
5.3 LLVM/Clang ................................ ................................ ................................ ..... 19 
5.4 OpenBSD regex ................................ ................................ ............................... 20 
6 Contact ................................ ................................ ................................ ........................ 22

### Page 5

Technical Reference MICROSAR Safe Silence Verifier 
2014, Vector Informatik GmbH Version: 1.4 
based on template version 4.11.3 
5 / 22 
Tables 
Table 2-1 Command Line Parameters ................................ ................................ ........ 8 
Table 3-1 Message classes and their value ................................ .............................. 13 
Table 4-1 Locations of Deliverables in an SIP ................................ .......................... 14

### Page 6

Technical Reference MICROSAR Safe Silence Verifier 
2014, Vector Informatik GmbH Version: 1.4 
based on template version 4.11.3 
6 / 22 
1 Introduction 
MICROSAR Safe Silence Verifier (MSS V) is a command line tool delivered as part of 
Silent BSW packages. MSSV checks based on rules the consistency of generated 
configuration files of the BSW modules. The result is written to a HTML report. The report 
is part of the proof that the BSW modules fulfill the Freedom from Interference criteria. 
 
 
Reference 
For all required steps to be performed as part of the Silent BSW integration see the 
project specific Safety Manual. 
 
1.1 Intended audience 
This document is relevant for developers who integrate Silent BSW into their ECU.

### Page 7

Technical Reference MICROSAR Safe Silence Verifier 
2014, Vector Informatik GmbH Version: 1.4 
based on template version 4.11.3 
7 / 22 
2 Functional Description 
This chapter describes the tool MSSV and how it can be used to check the consistency of 
the generated configuration data for SilentBSW modules. MSSV supports configuration via 
command line parameters. These are described in the following sectio n together with the 
report which is the output of MSSV. 
2.1 Required Environment 
MSSV supports the following operating systems: 
> Windows XP SP3 (32Bit) 
> Windows 7 (32Bit) 
> Windows 7 (64Bit) 
2.2 Restrictions 
MSSV uses a Compiler front end in order to compile the input source files. This Compiler 
front end requires ANSI -C 90 [1] conform source code. Some target compiler s implement 
specific language extensions which might prevent MSSV from compiling the code 
successfully. The Vector BSW code does not contain such language extensions. However, 
these extensions may be included via customer header files. In such a case the c ustomer 
shall take care that these language extensions are encapsulated via the prep rocessor for 
the MSSV execution. The corresponding preprocessor switches can be specified via the 
command line when calling MSSV. 
2.3 Command Line Parameters 
MSSV is configured by means of command line parameters. This chapter describes the 
available command line parameters and their meaning. 
Command Line Parameter Description 
Optional Parameters 
-h, --help Display available options. 
--version Prints the version and exits. 
-v, --verbose Enables verbose output of MSSV. 
--crcCheck Only perform CRC32 checks and then exit. 
--openReport Open the report file when finished. 
--stats Display timing statistics when MSSV is finished. 
-l, --logFile 

### Page 8

Technical Reference MICROSAR Safe Silence Verifier 
2014, Vector Informatik GmbH Version: 1.4 
based on template version 4.11.3 
8 / 22 
Command Line Parameter Description 
Optional Parameters 
If this parameter is missing MSSV writes the report to 
the current working directory. 
-p, --pluginDir <directory> Specifies the path of the plugin directory. By default 
this is the subfolder “plugins” in the directory of MSSV. 
-D, --define <symbol> Additional defines for the compiler. 
Required Parameters 
-i, --inputDir <directory> One or more input directories. 
Table 2-1 Command Line Parameters 
2.3.1 Option -h, --help 
This command line option prints the help of MSSV on the console. The help lists all 
command line parameters as displayed in Table 2-1. 
2.3.2 Option --version 
This parameter displays the version of MSSV on the command line. 
2.3.3 Option -v, --verbose 
The verbose option enables a verbose output of messages from MSSV. As a default the 
verbose mode is not active. This means that MSSV only displays warnings, errors and 
fatal errors as well as some selected note messages which might be of interest for the 
user. If the verbose mode is enabled MSSV will display all note messages. 
2.3.4 Option --crcCheck 
The CRC check option can be used to check the CRC32 checksums of the plugins. Then 
the report file contains a report about all plugins and their checksums. If the report is green 
all plugins are valid. If the report is red at least one plugin is invalid. 
2.3.5 Option --openReport 
This command line parameter instructs MSSV to open the resulting report HTML file after it 
has finished. Please make sure that HTML files are open ed with a suitable program by 
default when using this option (e.g. if you double click an HTML file in the explorer it should 


*Excerpt: first 8 of 22 pages shown.*
