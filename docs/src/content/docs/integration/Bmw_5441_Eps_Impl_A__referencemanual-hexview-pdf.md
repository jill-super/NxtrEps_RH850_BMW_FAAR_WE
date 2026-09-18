---
title: '_Bmw_5441_Eps_Impl_A — ReferenceManual_HexView'
description: 'Converted PDF document ReferenceManual_HexView.pdf from module _Bmw_5441_Eps_Impl_A.'
sidebar:
  hidden: true
---

> **Source:** `ReferenceManual_HexView.pdf` (PDF, 1728 KB, in-module path `doc/`)
>
> Converted from PDF with text extraction; layout, vector diagrams and scanned figures are not preserved. See the source PDF in the repository for the authoritative content.
>
> pages: 121; title: HexView; author: Armin Happel

## Converted content

### Page 1

Reference Manual HexView 
© 2017 Vector Informatik GmbH Version 1.11.01 1 
based on template version 5.1.0 
 
 
 
 
 
 
 
 
 
 
 
HexView 
Reference Manual 
 
 
Version 1.11.01 
 
 
 
 
 
 
 
 
 
 
Authors Armin Happel 
Status Released

### Page 2

Reference Manual HexView 
© 2017 Vector Informatik GmbH Version 1.11.01 2 
based on template version 5.1.0 
Document Information 
History 
Author Date Version Remarks 
Vishp 2006-02-21 1.0 > Creation 
Vishp 2006-07-14 1.1 > Description of new features for V1.2.0 
> Main features are: 
> Support for Ford-VBF and Ford-IHex in 
dialogs 
> Compare-Feature 
> Auto-detect file format on file open/save 
Vishp 2006-09-27 1.2 > Description of new features for V1.3.0 
> Merge and compare uses now the auto-
filetype detection 
> Merge operation available from 
commandline 
> Address calculation from banked to linear 
addresses from commandline 
> Checksum calculation feature from 
commandline places results into file or data. 
Vishp 2006-12-07 1.3 > Description of new features for V1.4.0 
> Commandline: Checksum operates on 
selected section. Multiple checksum areas 
can be specified from the commandline. 
> Postbuild operation added 
> Fixing Ford IHex configuration problem for 
flashindicator and File-Browse in the dialog 
> Option /CR (cut-section) added to the 
commandline 
> Delete and Cut&paste with internal 
clipboard added. 
> Description of the commandline processing 
order added to the document 
> Program returns a value depending on the 
status of operation 
> New option combination /XG with /MPFH to 
re-position existing NOAM to adjusted 
NOAR-fields 
> Goto start of a block (double-click to block 
descriptor) 
> Find ASCII string in data was added 
Vishp 2007-07-09 1.31 > Description of new features for V1.4.6 
> Support part number in GM-files (option /pn)

### Page 3

Reference Manual HexView 
© 2017 Vector Informatik GmbH Version 1.11.01 3 
based on template version 5.1.0 
from the commandline and reading the file 
Vishp 2007-09-19 1.4 > Description of new features for V1.5 
> Start CANflash from within Hexview 
> Create partial datafiles for Fiat-export 
> Support VBF V2.4 for Ford 
> Support Align Erase (/AE) 
> Use ranges instead of start and end address 
> Creation of a validation structure 
> New About-dialog with personalized license 
info 
Vishp 2008-01-31 1.5 > Fixing wrong description of checksum 
calculation for method 8 (see Table 3-3, 
index 8) 
Vishp 2009-05-19 1.6 > Description of new features for V1.6 
> Fixing problem when HEX-file contain 
addresses until 0xFFFF.FFFF 
> Extend expdatproc interface to allow 
insertion of data processing results into 
HEX-file 
> Now browse for data processing parameter 
file 
> Intel-HEX record length now adjustable 
> This document can now be opened from 
Help menu 
> Allow to select multiple post build files 
> Generate structured hex file from Eeprom 
data set 
> C-array generation supports structured list, 
Ansi-C and memmap. 
Vishp 2009-11-27 1.06.01 > Fixing problems with path names using a 
colon, e.g. “D:” 
> Minor corrections in the documentation 
(CRC calculation algorithms) 
Vishp 2010-10-11 1.06.04 > AccessParameter for Fiat export now 
editable. 
> Export binary blocks from commandline 
interface 
Vishp 2011-12-05 1.07.00 > Fixing Windows7 problems in dialogs. 
> Faster HEX read operation 
> Support dsPIC copy and ghost byte 
clearance 
> Export splitted binary data files per segment 
> Add checksum to last data bytes (@end)

### Page 4

Reference Manual HexView 
© 2017 Vector Informatik GmbH Version 1.11.01 4 
based on template version 5.1.0 
> Further support for compress+sign 
> Padding for data encryption 
> Scanning memory for EepM data (for 
development) 
> S5 records are now tolerated. 
> Swapping words or longwords 
Vishp 2012-09-15 1.08.00 > Solving further Win7 problems in dialogs. 
> Adding SHA256 in checksum and data 
processing DLL 
> Record type specifier in the commandline for 
Intel-HEX and Motorola S-Records. 
> Add import and Export for HEX ASCII data 
through commandline 
> Generate signature header for GM 
> Support for VBF V2.5 (Volvo) 
Vishp 2014-03-11 1.08.04 > Correcting padding mode for AES 
> Add support for IV-Vector w/ AES-CBC 
> Support for VBF V3.0 (Ford) 
> Improvements for the GM-header signature 
generation for cyber security. 
> Corrections on address range definition for 
data processing. 
> Ford-VBF allows now to omit the erase 
table. Editable now in the GUI. 
> Call to CANflash removed. 
> Description for validation structure 
generation added. 
> Support multiple part numbers for VBF 
> Merging files over commandline supports 
now wildcards. 
> Order of identifiers for VBF corrected. 
> Expdatproc V1.08.04 added 
> RSA encryption/decryption byte order 
corrected. 
> Padding mode for AES corrected 
> IV can be specified explicitly for AES 
CBC in the parameter 
Vishp 2014-04-07 1.08.05 > Commandline option to export MIME coded 
files 
Vishp 2014-05-19 1.08.06 > Export/Import of GAC binary files 
Vishp 2014-01-16 1.09.00 > Import and Export of MIME coded files 
(BASE64) 
> Correct description of /remap in the

### Page 5

Reference Manual HexView 
© 2017 Vector Informatik GmbH Version 1.11.01 5 
based on template version 5.1.0 
commandline overview 
> New expdatproc included, rework RSA 
encryption/decryption, crypto-library 
replaced with Vector crypto-lib.. 
> ARLE compression/decompression added. 
> Support GM compressed envelope 
> Incorrect length of imported MIME data 
> Wrong update of erase information in ini file 
for VBF 
> Message "out of memory" displayed when 
opening BIN-files 
> File type recognition failure with files that 
have no extensions 
> Checksum calculation over a fixed range, 
even if there are wholes in the internal data 
Commandline: /cs<csum-method-
number>:@<address>;!<range>|<fillpattern> 
Example: /cs9:@0x8000;!0x9000-
0xBFFF|CAFÉ 
Vishp 2015-04-13 1.09.01 > Validation struct inserted as separate block. 
> Support for VBF V4.0 
> Support splitting big block into smaller junks 
Vishp 2015-07-25 1.09.02 > Limited RSA operation with private key 
> Importing binary data over commandline 
> Improved ASCII import. 
> Hexview version reported in logfile. 
> Unknown commandline options reported in 
logfile. 
> Referencing alternative expdatproc.dll 
Vishp 2015-08-28 1.09.03 > Allow sw_version in VBF V2.5 with no char. 
> RSA operation with public key only fails. 
> 16-Bit Intel import doesn’t allow segment 
wrapping. 
Vishp 2016-01-21 1.09.04 > Correcting data processing operations. 
Vishp 2016-03-18 1.10.00 > MISRA and strict ANSI for C-File generation 
improved. 
> Extensions to expdatproc (RSA-PSS, RSA-
OAEP) 
> Hexview returned error codes even if no 
error was detected. 
> Checksum calculation over holes revised. 
> Support PKCS#1, PKCS#8 and X.509 
certificates as file input for RSA operations

### Page 6

Reference Manual HexView 
© 2017 Vector Informatik GmbH Version 1.11.01 6 
based on template version 5.1.0 
(without passwords). 
Vishp 2016-09-05 1.10.01 > Fixing dialog problem with HEX ASCII export 
> Allow long lines for HEX ASCII exports 
> Introduce /CSR for reverse csum output 
> Multiple modules for GM SLP4 export 
> DataTypes can be specified for GM cmpr. 
Sign. (envelope 3) 
> Value input with leading 0 no longer leads to 
interpretation of octal values. 
Vishp 2017-03-09 1.10.04 > Tag length calculation for validation structure 
corrected. 
> GM SLP5: Extend use of of cal-files from 20 
to 128. 
> Extend number of regions from 32 to 256. 
> Extend number of partitions from 20 to 128. 
> Allow usage of CAL module IDs from 51 to 
70. Removed them as application modules. 
Vishp 2017-06-09 1.11.00 > Switches /gmal and /gmad for separate GM 
header alignment operations 
> Support for further VCC VBF version. 
> Support for further Ford VBF version. 
> Support for ed25519 signature 
> Remove encryption from standard package 
due to BAFA export restricti

*Excerpt: first 8 of 121 pages shown.*
