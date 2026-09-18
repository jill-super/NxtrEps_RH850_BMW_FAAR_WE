---
title: 'TL102A_Davinci — ApplicationNotes_DifferenceAnalyzer'
description: 'Converted PDF document ApplicationNotes_DifferenceAnalyzer.pdf from module TL102A_Davinci.'
sidebar:
  hidden: true
---

> **Source:** `ApplicationNotes_DifferenceAnalyzer.pdf` (PDF, 371 KB, in-module path `doc/`)
>
> Converted from PDF with text extraction; layout, vector diagrams and scanned figures are not preserved. See the source PDF in the repository for the authoritative content.
>
> pages: 18; title: Microsoft Word - ApplicationNotes_DifferenceAnalyzer.doc; author: viscs

## Converted content

### Page 1

DaVinci Difference Analyzer 
Application Note 
 
 
 
 
Version 1.7 
 
 
 
 
 
 
Authors: Stefanie Kruse, Matthias Wernicke, Andreas 
Claus, Daniel Fürderer 
Version: 1.7 
Status: released

### Page 2

DaVinci Difference Analyzer Application Note 
 2015, Vector Informatik GmbH Version: 1.7 
 
History 
 
Author Date Version Remarks 
Ske 2009-05-20 1.0 Initial version 
Ske 2009-06-10 1.1 Description of starting DaVinci Difference Analyzer enhanced 
Wk 2009-07-29 1.2 Document restructured and completed 
Cs 2011-06-28 1.3 Description of filter options added 
Dfr 2012-01-24 1.4 Updated figures and added description of view options (3.6), 
Parent Path (3.7) and DPA compare (3.8) 
Cs 2012-05-02 1.5 Additional Copyrights added 
Dfr 2014-01-28 1.6 Added description of ‘Filter equal elements’ option (3.5.2 and 4) 
Cs 2015-05-28 1.7 Usage of Saxon-PE distributable package

### Page 3

DaVinci Difference Analyzer Application Note 
 2015, Vector Informatik GmbH Version: 1.7 
 
Contents 
1 Overview ............................................................................................. ...................... 5 
2 Installation ......................................................................................... ....................... 6 
2.1 Setup program ........................................................................................ .... 6 
2.2 Licensing ............................................................................................ ........ 6 
3 Using DaVinci Difference Viewer ...................................................................... ....... 7 
3.1 Starting the difference analysis ................................................................... 7 
3.2 Display of the differences ........................................................................... 8 
3.3 Saving the result of a difference analysis .................................................... 9 
3.4 Opening the result file of a difference analysis ............................................ 9 
3.5 Filter Options ....................................................................................... ....... 9 
3.5.1 Element Identification ............................................................................... 10 
3.5.2 Filter equal elements ................................................................................ 11 
3.5.3 Element Filter ....................................................................................... .... 11 
3.5.4 Loading/Storing Options ........................................................................... 11 
3.6 View Options .........................................................................

### Page 4

DaVinci Difference Analyzer Application Note 
 2015, Vector Informatik GmbH Version: 1.7 
 
7 Contact .............................................................................................. ...................... 18

### Page 5

DaVinci Difference Analyzer Application Note 
 2015, Vector Informatik GmbH Version: 1.7 
 
1 Overview 
This document explains the usage of the command lin e tool “DaVinci Difference Analyzer” 
Version 2.7 and tells how to interpret the result. 
 
DaVinci Difference Analyzer compares two ARXML file s and puts the result into a result 
file. Additionally you can compare two DaVinci Proj ect Assistant projects by their DPA 
files. For further information on DPA compare see chapter 3.8.

### Page 6

DaVinci Difference Analyzer Application Note 
 2015, Vector Informatik GmbH Version: 1.7 
 
2 Installation 
2.1 Setup program 
The DaVinci Difference Analyzer can be installed by starting the setup program 
DaVinciDiff.msi. This setup is part of a DaVinci to ol setup and is installed during the tool 
installation procedure. 
The DaVinci Difference Analyzer is installed into one of the following folders: 
n English Windows: C:\Program Files\Common Files\Vector 
n German Windows: C:\Programme\Gemeinsame Dateien\Vector 
The following executables are installed in the sub-folder “DiffAnalyzer”: 
n DVDiffSys.exe: Command line program for comparing AUTOSAR XML files 
(System Description files, Software Component Description files or ECU 
Configuration Description files) 
n DVDiffView.exe: Program for displaying the differences between two AUTOSAR 
XML files 
2.2 Licensing 
In order to run DaVinci Difference Analyzer a license of at least one of the following tools is 
required on the PC: 
n DaVinci Configurator Pro 
n DaVinci Developer

### Page 7

DaVinci Difference Analyzer Application Note 
 2015, Vector Informatik GmbH Version: 1.7 
 
3 Using DaVinci Difference Viewer 
3.1 Starting the difference analysis 
The difference analysis can be started via one of the following options 
 
n Via the Program menu 
Using Program menu | <DaVinci tool, e.g. Vector DaVinci Configurator 4.0> 
| DaVinci Difference Viewer the DaVinci Difference Viewer is started. Using 
File | New you can open a dialog for selecting the two AUTOSAR XML files to 
be compared. After confirming this dialog, the comparison is started and the 
differences are displayed. 
n Via the Windows Explorer 
After selecting two files with extension .arxml in the Windows Explorer, you can 
display the differences between these files using the context menu entry 
AUTOSAR XML Diff 
 
 
Figure 1: Analyze two files with the shell extension of DaVinci Difference Analyzer 
 
Alternatively, you can select the first file, use the context menu entry Select as left 
side for AUTOSAR XML Diff

### Page 8

DaVinci Difference Analyzer Application Note 
 2015, Vector Informatik GmbH Version: 1.7 
 
 
Figure 2: Select source file to compare AUTOSAR files with the DaVinci Difference Analyzer 
 
 
and then select the second file and context menu entry AUTOSAR XML Diff with 
 
 
Figure 3: Shell Extension of DaVinci Difference Analyzer 
3.2 Display of the differences 
The differences are displayed in the DaVinci Differ ence Viewer (Figure 4: DaVinci 
Difference Viewer).

*Excerpt: first 8 of 18 pages shown.*
