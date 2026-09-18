---
title: 'CM102A_FlsMem_Impl — FlsMem Module Design Document'
description: 'Converted Word (.docx) document FlsMem Module Design Document.docx from module CM102A_FlsMem_Impl.'
sidebar:
  hidden: true
---

> **Source:** `FlsMem Module Design Document.docx` (Word (.docx), 266 KB, in-module path `doc/`)
>
> Converted from OOXML (`word/document.xml`); headings, lists and tables preserved. Embedded objects and images are inventoried below.
>
> props: {'title': 'Module Design Document', 'creator': 'Windows User', 'subject': '', 'keywords': '', 'description': ''}; embedded images: 3 (emf, png); OLE embeddings: 1; tables converted: 6

## Converted content

For

FlsMem

Sep 19 , 2017

Prepared For:

Software Engineering

Nexteer Automotive,

Saginaw, MI, USA

Prepared By:

Software Group,

Nexteer Automotive,

Saginaw, MI, USAChange History



| Description | Author | Version | Date |

| --- | --- | --- | --- |

| Initial Version | Lucas Wendling | 1.0 | 10/06/15 |

| Updated with changes for DTS configuration for Flash CRC check | Avinash James | 2.0 | 03/18/16 |

| Updates for DTS Transfer Clear | Avinash James | 3.0 | 3/29/16 |

| Updated for removing the flash ECC single bit error handling and disabling the DTS channels after calculation | Avinash James | 4.0 | 3/31/16 |

| Trusted function call for the DTS clean up updates | Avinash James | 5.0 | 04/18/16 |

| Function name changes and added CodFlsSngBitEcc handler for single bit code flash ecc | Avinash James | 6.0 | 08/25/16 |

| Updated to design version 7.1.0 | Avinash James | 7.0 | 04/10/17 |

| Updated to include design limitations | Avinash James | 8.0 | 09/19/17 |



Table of Contents1Introduction5

1.1Purpose5

1.2Scope5

2FlsMem & High-Level Description6

3Design details of software module7

3.1Graphical representation of FlsMem7

3.2Data Flow Diagram7

3.2.1Component level DFD7

3.2.2Function level DFD7

4Constant Data Dictionary8

4.1Program (fixed) Constants8

4.1.1Embedded Constants8

5Variable Data Dictionary9

5.1User defined typedef definition/declaration9

5.2Variable definition for enumerated types9

6Software Component Implementation10

6.1Sub-Module Functions10

6.1.1Init: FlsMemInit110

6.1.1.1Design Rationale10

6.1.1.2Module Outputs10

6.1.2Init: FlsMemInit210

6.1.2.1Design Rationale10

6.1.2.2Module Outputs10

6.1.3Per: FlsMemPer210

6.1.3.1Design Rationale10

6.1.3.2Store Module Inputs to Local copies10

6.1.3.3(Processing of function)………10

6.1.3.4Store Local copy of outputs into Module Outputs10

6.2Server Runnables11

6.3Interrupt Functions11

6.4Module Internal (Local) Functions11

6.4.1Local Function #111

6.4.1.1Design Rationale11

6.4.1.2Processing11

6.5GLOBAL Function/Macro Definitions11

6.5.1DTSInit11

6.5.1.1Design Rationale11

6.5.1.2Processing14

6.5.2DTSClnUp14

6.5.2.1Design Rationale14

6.5.2.2Processing14

7Known Limitations with Design15

8UNIT TEST CONSIDERATION16

Appendix AAbbreviations and Acronyms17

Appendix BGlossary18

Appendix CReferences19

## Introduction

### Purpose

### Scope

The following definitions are used throughout this document:

Shall: indicates a mandatory requirement without exception in compliance.

Should: indicates a mandatory requirement; exceptions allowed only with documented justification.

May: indicates an optional action.

## FlsMem & High-Level Description

See FDD

## Design details of software module

### Graphical representation of FlsMem

### Data Flow Diagram

#### Component level DFD

See FDD

#### Function level DFD

See FDD

## Constant Data Dictionary

### Program (fixed) Constants

#### Embedded Constants

#### Local Constants



| Constant Name | Resolution | Units | Value |

| --- | --- | --- | --- |

| CPU1PEID_CNT_U32 | 1 | uint32 | 0x01U |

| CODFLSTOCRCSPID_CNT_U32 | 1 | uint32 | 0x02U |

| CRCTOLCLRAMSPID_CNT_U32 | 1 | uint32 | 0x00U |

| USRMODDIS_CNT_U32 | 1 | uint32 | 0x00U |

| FLSBLKLEN_CNT_U32 | 1 | uint32 | 0x0003FFFCU |

| DTSDATALEN_CNT_U32 | 1 | uint32 | 4U |

| CRCCHKMAXALLWDTI_CNT_U32 | 1 | uint32 | 2000 |

| MAXNROFDTSCH_CNT_U32 | 1 | uint32 | 32 |

| TOUTCRCCALCN_CNT_U08 | 1 | uint08 | 0xFFU |

| READADRCASE0_CNT_U08 | 1 | uint08 | 0 |

| READADRCASE1_CNT_U08 | 1 | uint08 | 1 |

| READADRCASE2_CNT_U08 | 1 | uint08 | 2 |

| READADRCASE3_CNT_U08 | 1 | uint08 | 3 |

| ERRADRMASK_CNT_U32 | 1 | Uint32 | ((uint32)0x80UL) |

| NROFADRCHK_CNT_U08 | 1 | uint08 | ((uint8)4U) |



## Variable Data Dictionary

### User defined typedef definition/declaration

<This section documents any user types uniquely used for the module.>



| Typedef Name | Element Name | User Defined Type | Legal Range (min) | Legal Range (max) |

| --- | --- | --- | --- | --- |

| FlsCrcCfgBlkRec | CrcFlsBlkStrtAdr | uint32 | 0 | 0xFFFFFFFFH |

|  | CrcFlsBlkLen | uint32 | 0 | 0xFFFFFFFFH |

|  | PreCalcnCrcFlsAdr | uint32* | 0 | 0xFFFFFFFFH |



### Variable definition for enumerated types



| Enum Name | Element Name | Value |

| --- | --- | --- |

| <(Name given for the user defined typdef of type struct/union) (Variable name qualified in refer[2])> | <(Variable name qualified Refer[2])> | <Define the value > |



## Software Component Implementation

### Sub-Module Functions

### Init: FlsMemInit1

### Design Rationale

Function to return the application region CRC to Diag Manager

### Module Outputs

None

### Init: FlsMemInit2

### Design Rationale

The FlsMemInit2 function is a non RTE function which shall be called to set up the DTS configuration for the Flash CRC check. The DTS channel configuration has to be applied only when the system is waking up from a Power On Reset or after a flash programming reset. In such a scenario a Hardware CRC unit is allocated by function call to the CRC module and once a hardware assignment is successful, the DTS channels are configured for chaining for the entire definition of the flash blocks (Boot, App, Cal1, Cal2 etc.). Record the time when the DTS transfer is initiated so that a check on a timeout can be made in the periodic function where a maximum timeout of 200 ms is checked for

This function shall be called in the startup sequence. Hence it is a non RTE function

See FDD for more.

### Module Outputs

None

None

### Per: FlsMemPer2

### Design Rationale

See FDD

### Store Module Inputs to Local copies

Refer to FDD

### (Processing of function)………

Refer to FDD

### Store Local copy of outputs into Module Outputs

Refer to FDD

### Server Runnables - CodFlsSngBitEcc

### Design Rationale

See FDD

### Store Module Inputs to Local copies

Refer to FDD

### (Processing of function)………

Refer to FDD

### Store Local copy of outputs into Module Outputs

Refer to FDD

### Interrupt Functions

None

### Module Internal (Local) Functions

### Local Function #1



| Function Name | (Exact name used) | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | None | <Refer MDD guidelines[1]> | <Refer MDD guidelines[1]> | <Refer MDD guidelines[1]> |

| Return Value |  |  |  |  |



### Design Rationale

### Processing

### GLOBAL Function/Macro Definitions

### DtsInin



| Function Name | DTSInit | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | CrcHwIdxInReg | uint32 | 0 | 0xFFFFFFFF |

|  | CrcHwIdxOutReg | uint32 | 0 | 0xFFFFFFFF |

| Return Value | None |  |  |  |



### Design Rationale

Trusted function that performs all register initialization from the CM102A_FlsMem_DTSPeripheralCfg.xlsx spreadsheet in the FDD.  The DTSMstrCfg channel master registers can be written only in supervisor mode.  After the Channel master register for a given channel has been written, the selected Processor Element can write to that channel’s registers.  However, for simplicity, all DTS register initialization and chaining is being done in one trusted function.

The chaining is done in the following manner

- Consider the first flash region to have the CRC calculated

- Calculate the number of DTS chains required for the length of the CRC region. Each DTS channel can address up to a maximum of 0x3FFFC bytes of data (0xFFFF maximum transfer count multiplied by 4 bytes of data in each transfer).

Hence number of channel is equal to Region length/0x3FFFC + {1} if (Region length % 0x3FFFC is non zero)

- Clear the DTS Transfer flag to make sure no pending requests are present for all the used channels

- Configure the DTS channels starting from 0 using the configuration defined as per CM102A_FlsMem_DTSPeripheralCfg.xlsx for the above calculated number of chains

- Configure the next DTS channel to transfer the CRC result from CRC HW output register to Per Instance Memory

- Configure the next DTS channel t

*Body truncated: document is longer than the excerpt shown here.*
