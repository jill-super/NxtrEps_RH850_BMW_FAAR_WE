---
title: '_Bmw_5441_Eps_Impl_A — TechnicalReference_SipModificationChecker'
description: 'Converted PDF document TechnicalReference_SipModificationChecker.pdf from module _Bmw_5441_Eps_Impl_A.'
sidebar:
  hidden: true
---

> **Source:** `TechnicalReference_SipModificationChecker.pdf` (PDF, 437 KB, in-module path `doc/`)
>
> Converted from PDF with text extraction; layout, vector diagrams and scanned figures are not preserved. See the source PDF in the repository for the authoritative content.
>
> pages: 11; title: SIP Modification Checker; author: Markus Schwarz

## Converted content

### Page 1

SIP Modification Checker 
Technical Reference 
 
 
Version 1.00.00 
 
 
 
 
 
 
 
 
 
 
 
Authors Markus Schwarz 
Status Released

### Page 2

Technical Reference SIP Modification Checker 
2014, Vector Informatik GmbH Version: 1.00.00 
based on template version 5.7.1 
2 / 11 
Document Information 
History 
Author Date Version Remarks 
Markus Schwarz 2014-05-07 1.00.00 Initial version 
 
Reference Documents 
No. Source Title Version 
[1] 
Scope of the Document 
This technical reference describes the general use of the tool SipModificationChecker.

### Page 3

Technical Reference SIP Modification Checker 
2014, Vector Informatik GmbH Version: 1.00.00 
based on template version 5.7.1 
3 / 11 
Contents 
1 Component History ................................ ................................ ................................ ...... 5 
2 Introduction................................ ................................ ................................ ................... 6 
2.1 Overview ................................ ................................ ................................ ............ 6 
2.2 Background ................................ ................................ ................................ ........ 6 
2.3 Workflow ................................ ................................ ................................ ............ 7 
2.3.1 At Vector ................................ ................................ ............................ 7 
2.3.2 At Tier1/OEM ................................ ................................ ..................... 7 
3 Functional Description ................................ ................................ ................................ . 8 
3.1 Command Line Usage ................................ ................................ ....................... 8 
3.1.1 Console Output ................................ ................................ .................. 8 
3.1.2 Return Error Codes ................................ ................................ ............ 8 
3.1.3 Report Creation ................................ ................................ .................. 9 
3.2 Integration ................................ ................................ ................................ .......... 9 
4 Glossary and Abbreviations ................................ ......................

### Page 4

Technical Reference SIP Modification Checker 
2014, Vector Informatik GmbH Version: 1.00.00 
based on template version 5.7.1 
4 / 11 
Illustrations 
Figure 2-1 Workflow at Vector ................................ ................................ ...................... 7 
Figure 2-2 Workflow at Tier1/OEM ................................ ................................ ............... 7 
 
Tables 
Table 1-1 Component history................................ ................................ ...................... 5 
Table 3-1 Command Line ErrorCodes ................................ ................................ ........ 8 
Table 7-1 Glossary ................................ ................................ ................................ ... 10 
Table 7-2 Abbreviations ................................ ................................ ............................ 10

### Page 5

Technical Reference SIP Modification Checker 
2014, Vector Informatik GmbH Version: 1.00.00 
based on template version 5.7.1 
5 / 11 
1 Component History 
The component history gives an overview over the important milestones that are 
supported in the different versions of the component. 
Component Version New Features 
1.00.00 Initial Version 
 
Table 1-1 Component history

### Page 6

Technical Reference SIP Modification Checker 
2014, Vector Informatik GmbH Version: 1.00.00 
based on template version 5.7.1 
6 / 11 
2 Introduction 
This document describes the functionality of the tool SipModifcationChecker. 
2.1 Overview 
The SipModifcationChecker is a tool that supports the Tier1 and OEM to determine if and 
where the (source code) files delivered from Vector were unintentionally changed. 
The SipModifcationChecker 
> is a command line based tool. 
> checks sources below a user-selectable root directory against information given in a 
reference file. 
> checks if and which of the relevant delivered files are contained below that directory. 
> checks if and which files have been modified. 
> reports the “modification state” as ERRORLEVEL and within a HTML report. 
2.2 Background 
This tool aims to find changes that were unintendedly introduced by the customer in the 
delivered Vector source code.

### Page 7

Technical Reference SIP Modification Checker 
2014, Vector Informatik GmbH Version: 1.00.00 
based on template version 5.7.1 
7 / 11 
2.3 Workflow 
2.3.1 At Vector 
> Vector creates the list of relevant files, i.e. all (source code) files that are relevant to 
not be modified 
> Vector calculates a check code for each of these files and creates the 
SipCheckCodeFile 
> Vector delivers the embedded sources, the SipCheckCodeFile and the 
SipModifcationChecker 
 
Figure 2-1 Workflow at Vector 
2.3.2 At Tier1/OEM 
> The Tier1/OEM run the SipModifcationChecker, configure their root path and load the 
SipCheckCodeFile from Vector. The tool provides information if the local sources found 
below the selected root directory are un-modified. 
 
Figure 2-2 Workflow at Tier1/OEM 
WP
SourceCode
Tool
SipModifcationChecker
SipCheckCodeFile
Deliv ery
Vector
WP
RelevantFiles
«create»
«based on»
+SubSet
WP
SourceCode
Tool
SipModifcationChecker
SipCheckCodeFile
Deliv ery
Customer
WP
UsedSourceCode
«use»
check for modification
+CurrentCode
+Reference

### Page 8

Technical Reference SIP Modification Checker 
2014, Vector Informatik GmbH Version: 1.00.00 
based on template version 5.7.1 
8 / 11 
3 Functional Description 
3.1 Command Line Usage 
The analysis can be executed from command line. 
Syntax: 
SipModificationChecker <rootPath> <referenceFile> 
rootPath: path to the directory that is used as base for analysis 
referenceFile: path to the provided reference file 
 
Example: 
SipModificationChecker c:\Example\CodeRootPath 
C:\Example\SipModificationChecker.xml 
 
If the rootPath or the referenceFile do not exist, the tool outputs a command line message 
and returns a ProcessError. 
Otherwise the tool checks all files provided in referenceFile if they can be found below the 
rootPath and if they have local modifications compared to the delivery. 
 
3.1.1 Console Output 
The tool outputs the results in the console: 
=> Result: 
 115/310 files are OK (unmodified) 
 185/310 files are NOT OK (i.e. they have been modified) 
 10/310 files are not found in given directory 
 Refer to HTML for details 
=> ERROR 
 
3.1.2 Return Error Codes 
The tool sets the environmental variable ERRORLEVEL depending on its result: 
Return Code Value Description 
Ok 0 All referenced files are found. 
They have no modifications. 
Warning 1 Not all referenced files are found. 
All found files have no modifications. 
Error 10 There is at least one file with modifications. 
ProcessError 20 The check could not be performed as the input data is not valid 
(rootPath and/or referenceFile do not exist) 
Table 3-1 Command Line Error Codes

*Excerpt: first 8 of 11 pages shown.*
