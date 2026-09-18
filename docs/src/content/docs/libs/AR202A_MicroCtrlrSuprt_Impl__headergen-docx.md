---
title: 'AR202A_MicroCtrlrSuprt_Impl — HeaderGen'
description: 'Converted Word (.docx) document HeaderGen.docx from module AR202A_MicroCtrlrSuprt_Impl.'
sidebar:
  hidden: true
---

> **Source:** `HeaderGen.docx` (Word (.docx), 814 KB, in-module path `doc/`)
>
> Converted from OOXML (`word/document.xml`); headings, lists and tables preserved. Embedded objects and images are inventoried below.
>
> props: {'title': '', 'creator': 'daniel.sisco@renesas.com', 'subject': 'Rev. 1.2', 'keywords': 'April 20th, 2016', 'description': ''}; embedded images: 27 (emf, jpeg, png, wmf); OLE embeddings: 1; tables converted: 5

## Converted content

Rev. 1.2April 20th, 2016Rev. 1.2April 20th, 2016

Introduction

This document describes installation and usage of the C code header file generation script (HeaderGen) created by Renesas. The HeaderGen script is a Python based script that utilizes one external Python module for parsing Excel files. The purpose of the tool is to enable more configurable and consistent header file generation for our customers, as well as to provide some useful formatting options within the header files themselves.

## Installation

The following tools are needed for execution of the Script



| Tool | Version | Install instructions |

| --- | --- | --- |

| Python | v2.7.9 | Visit the Python Install site and download the latest v2.x.x Windows version: https://www.python.org/downloads/ |

| openpyxl | v2.3.0 | (1) Download easy_install from Windows from this link: https://bootstrap.pypa.io/ez_setup.py (2) execute the file ez_setup.py: (3) Navigate to C:\PythonXX\Script and execute . |

| Excel | 2013 | Script requires use of the .xlsx Excel file format |



Table 1: Required SW Packages

## Usage

### Configuration File

The script takes as an input a text configuration file. Required fields in the file are:



| Field | Description | Example |

| --- | --- | --- |

| Input_file_name | Excel input file name and full or relative path | ./dr7f701310_matrix_smaller.xlsx |

| Tab_name | Excel tab name with relevant data – typically “APB area2” | APB area2 |

| Output_file_location | Location where the resulting header files will be written with full or relative path. NOTE: this is currently unsupported | ./ |

| Base_type_byte | Base type for byte variables | uint8 |

| Base_type_short | Base type for short (two byte) variables | uint16 |

| Base_type_long | Base type for long (four byte) type variables | uint32 |

| Base_union_name_byte | Name for byte variable access within union of register access types | UINT8 |

| Base_union_name_short | Name for short variable access within union of register access types | UINT16 |

| Base_union_name_long | Name for long variable access within union of register access types | UINT32 |

| Base_union_name_bits | Name for bit variable access within union of register access types. This will provide access to the bitfield structure. | BITS |

| [prefix] (sample text) | Anything following a line starting with [prefix] will be printed exactly at the start of the header file, after the inclusion guard #ifdef |  |

| [groups] (sample group) | By default, all register access structures, address binding pragmas, and access macros will be placed into the default output file. Adding a group to the configuration file will place any register whose name starts with the text following [groups] into a separate file. More than one piece of text can follow a group name, as shown in the example. | [groups] ADC_FILE = ADCD0, ADCD1 This will place all registers starting with either “ADC0” or “ADCD1” into an output file called dr7f701310_ADC_FILE.h, and cause them to skip the default header file. [groups] DEFAULT = This is the default group for all register information. It must be present in the configuration file. This will place all unmatched registers into an output file called dr7f701310_DEFAULT.h. |

| [suffix] (sample text) | Anything following a line starting with [suffix] will be printed exactly at the end of the header file, before the inclusion guard #endif |  |

| [skip] (address) | Only hexadecimal addresses are allowed to follow the [skip] tag. Any register whose address overlaps with this address will be placed into a group labeled “skip” and generate into a _SKIP.h file | [skip] DEADBEEF |

| use_module_names = <True/False> | Setting this argument to true will ignore all [groups] arguments and use the module column from the Excel file as register grouping names. | use_module_names = True |

| gen_address_macros = <True/False> | Setting this argument to true will generate macros for each register mapping their address to the register name followed by “_ADDR” | gen_address_macros = True |



Table 2: configuration file entries

### Execution

The script can be executed by issuing this command from the command line:



| > python headerGen.py config.txt |

| --- |



Note: this assumes (1) the python executable has been added to your system path, and (2) the headerGen,py script and config file are resident in your current directory.

The script will print several informative messages to the command line as it runs. Because the Excel file for a typical micro is very large (>50,000 lines), the script can take up to 10 minutes to execute. It will print percentage complete status messages during long running sections.

You will see these messages when the command line script has completed:

### Output

Figure 1: header file contents and usage

## Revision Record



| Rev. | Date | Description |  |

| --- | --- | --- | --- |

|  |  | Page | Summary |

| 1.0 | 2/8/2016 | All | Initial Draft |

| 1.1 | 2/25/2016 | Multiple | Adding support for multiple groups, marking output file directory config option as unsupported. |

| 1.2 | 4/20/2016 | Multiple | Adding support for register address macro generation as well as register grouping based on module name column from Excel |



## Testing

Due to the size of the input Excel file, it is not feasible for Renesas or a customer (user) of the script to test each of the registers generated. Therefore, we have identified a sub-set of registers that represent interesting register layout permutations for testing. As long as these registers have generated fine, we can assume that all other register, being of identical pattern to these registers, are fine as well.

The registers in the test suite are:



| Number | Register size | Base access type | Bit access type | P1M example |

| --- | --- | --- | --- | --- |

| 1 | 8-bit | 8-bit | 8-bit | 15.3.10 – SCI30BRR |

| NOTE: SCI30BRR and SCI30MDDR are allocated to the same address, so the script will parse this incorrectly. |  |  |  |  |

| 2 | 8-bit | 8-bit | < 8-bit, single | 10.4.2 – CVMF |

| 3 | 8-bit | 8-bit | < 8-bit, multiple | 16.3.2.1 – RLN30LWBR |

| 3a | 8-bit | 8-bit, 1-bit | < 8-bit, single | 14.3.2 – CSIH0CTL0 |

| 4 | 16-bit | 16-bit | 16-bit | 13.3.10 – CSIG0TX0H |

| 5 | 16-bit | 16-bit | 8-bit | 16.3.3.18 – RLN30LUTDR |

| 6 | 16-bit | 16-bit | < 8-bit, single | 13.3.6 – CSIG0STCR0 |

| 7 | 16-bit | 16-bit | < 8-bit, multiple, cross byte boundaries | 13.3.4 – CSIG0CTL2 |
