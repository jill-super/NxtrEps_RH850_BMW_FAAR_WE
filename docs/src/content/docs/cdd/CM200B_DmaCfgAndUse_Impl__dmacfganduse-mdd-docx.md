---
title: 'CM200B_DmaCfgAndUse_Impl — DmaCfgAndUse_MDD'
description: 'Converted Word (.docx) document DmaCfgAndUse_MDD.docx from module CM200B_DmaCfgAndUse_Impl.'
sidebar:
  hidden: true
---

> **Source:** `DmaCfgAndUse_MDD.docx` (Word (.docx), 101 KB, in-module path `doc/`)
>
> Converted from OOXML (`word/document.xml`); headings, lists and tables preserved. Embedded objects and images are inventoried below.
>
> props: {'title': 'Module Design Document', 'creator': 'Spencer, Brionna', 'subject': '', 'keywords': '', 'description': ''}; embedded images: 2 (png); OLE embeddings: 0; tables converted: 8

## Converted content

For

DmaCfgAndUse

Version: 4.0

Release Date: 19-Feb-2018

Prepared For:

Software Engineering,

Nexteer Automotive,

Saginaw, MI, USA

Prepared By:

SEPG,

Nexteer Automotive,

Saginaw, MI, USA

Document Change History



| Version | Description | Author | Date |

| --- | --- | --- | --- |

| 1.0 | Initial Version | Avinash James | 27-May-2016 |

| 2.0 | Updated for corrected timing | Avinash James | 08-Jun-2016 |

| 3.0 | Updated as per Design 3.0.0 | Krzyszotf Byrski | 05-Dec-2017 |

| 4.0 | Updated design limitations and document template | Brionna Spencer | 19-Feb-2018 |



Table of Contents

1DmaCfgAndUse & High-Level Description5

2Design details of software module6

2.1Graphical representation of DmaCfgAndUse6

2.2Data Flow Diagram6

2.2.1Component level DFD6

2.2.2Function level DFD6

3Constant Data Dictionary7

3.1Program (fixed) Constants7

3.1.1Embedded Constants7

4Software Component Implementation8

4.1Sub-Module Functions8

4.1.1Init: DmaCfgAndUseInit18

4.1.1.1Design Rationale8

4.1.1.2Module Outputs8

4.1.2Per: DmaCfgAndUsePer18

4.1.2.1Design Rationale8

4.1.2.2Store Module Inputs to Local copies8

4.1.2.3(Processing of function) …8

4.1.2.4Store Local copy of outputs into Module Outputs8

4.2Server Runnables8

4.2.1DmaEna2MilliSecToMotCtrlTrf8

4.2.1.1Design Rationale8

4.2.1.2(Processing of function) …8

4.2.2DmaWaitForMotCtrlTo2MilliSecTrf8

4.2.2.1Design Rationale8

4.2.2.2(Processing of function) …9

4.2.3MotAg0SnsrCfgDmaStrt9

4.2.3.1Design Rationale9

4.2.3.2(Processing of function) …9

4.3Interrupt Functions9

4.4Module Internal (Local) Functions9

4.5GLOBAL Function/Macro Definitions9

4.5.1GLOBAL Function #19

4.5.1.1Design Rationale9

4.5.1.2Processing9

4.5.2GLOBAL Function #29

4.5.2.1Design Rationale9

4.5.2.2Processing10

4.5.3GLOBAL Function #310

4.5.3.1Design Rationale10

4.5.3.2Processing10

5Known Limitations with Design11

6UNIT TEST CONSIDERATIONS12

Appendix AAbbreviations and Acronyms13

Appendix BGlossary14

Appendix CReferences15

## DmaCfgAndUse & High-Level Description

DMA Configuration and Usage (DmaCfgAndUse) sets up the initial DMA configuration and defines the periodic and server runnable functionality needed for DMA transfers of SPI, ADC, and Motor Control loop/RTE interface data.

## Design details of software module

### Graphical representation of DmaCfgAndUse

### Data Flow Diagram

#### Component level DFD

None

#### Function level DFD

None

## Constant Data Dictionary

### Program (fixed) Constants

#### Embedded Constants

#### Local Constants



| Constant Name | Resolution | Units | Value |

| --- | --- | --- | --- |

| CPU1PEID_CNT_U32 | 1 | Counts | 1 |

| PRPHLTOLCLRAMSPID_CNT_U32 | 1 | Counts | 3 |

| LCLRAMTOPRPHLSPID_CNT_U32 | 1 | Counts | 2 |

| LCLRAMTOLCLRAMSPID_CNT_U32 | 1 | Counts | 0 |

| USRMODENA_CNT_U32 | 1 | Counts | 1 |

| USRMODDI_CNT_U32 | 1 | Counts | 1 |

| DMACFGANDUSE_MAXWAIT_MICROSEC_U32 | 1 | MicroSec | 400 |

| INIZERO_CNT_U32 | 1 | Counts | 0 |



Also see FDD DataDict.m file for constant definitions.

## Software Component Implementation

### Sub-Module Functions

### Init: DmaCfgAndUseInit1

### Design Rationale

The DMACnnCM channel master registers can be written only in supervisor mode. After the Channel master register for a given channel has been written, the selected Processor Element can write to that channel’s registers in user mode. However, for simplicity, all DMA register initialization is being done in one trusted function. Therefore, only the Per Instance Memory initialization is done directly in the DmaCfgAndUseInit1 function; all DMA register initialization is done in the DmaRegInin function called by DmaCfgAndUseInit1.

### Module Outputs

Refer to FDD

### Per: DmaCfgAndUsePer1

### Design Rationale

None

### Store Module Inputs to Local copies

None

### (Processing of function) …

Refer to FDD

### Store Local copy of outputs into Module Outputs

None

### Server Runnables

### DmaEna2MilliSecToMotCtrlTrf

### Design Rationale

None

### (Processing of function) …

None

### DmaWaitForMotCtrlTo2MilliSecTrf

### Design Rationale

None

### (Processing of function) …

None

### MotAg0SnsrCfgDmaStrt

### Design Rationale

None

### (Processing of function) …

None

### Interrupt Functions

None

### Module Internal (Local) Functions

None

### GLOBAL Function/Macro Definitions

### GLOBAL Function #1



| Function Name | DmaRegInin | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | None |  |  |  |

| Return Value | N/A |  |  |  |



### Design Rationale

Trusted function that performs all register initialization from the CM200B_DmaCfgAndUse_PeripheralCfg.xlsx spreadsheet in the FDD. The DMACnnCM channel master registers can be written only in supervisor mode. After the Channel master register for a given channel has been written, the selected Processor Element can write to that channel’s registers in user mode. However, for simplicity, all DMA register initialization is being done in one trusted function. For timing optimization, register level initialization is used (rather than bit field modifications of the register fields).

### Processing

Refer to FDD

### GLOBAL Function #2



| Function Name | InjDmaErr | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | None |  |  |  |

| Return Value | N/A |  |  |  |



### Design Rationale

Refer to FDD

### Processing

Refer to FDD

### GLOBAL Function #3



| Function Name | InjMcuDiagcErr | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | None |  |  |  |

| Return Value | N/A |  |  |  |



### Design Rationale

Refer to FDD

### Processing

Refer to FDD

## Known Limitations with Design

None

## UNIT TEST CONSIDERATIONS

None

#### Abbreviations and Acronyms



| Abbreviation or Acronym | Description |

| --- | --- |

| MDD | Module Design Document |

| DFD | Data Flow Diagram |



#### Glossary

Note: Terms and definitions from the source “Nexteer Automotive” take precedence over all other definitions of the same term.  Terms and definitions from the source “Nexteer Automotive” are formulated from multiple sources, including the following:

- ISO 9000

- ISO/IEC 12207

- ISO/IEC 15504

- Automotive SPICE® Process Reference Model (PRM)

- Automotive SPICE® Process Assessment Model (PAM)

- ISO/IEC 15288

- ISO 26262

- IEEE Standards

- SWEBOK

- PMBOK

- Existing Nexteer Automotive documentation



| Term | Definition | Source |

| --- | --- | --- |

| MDD | Module Design Document |  |

| DFD | Data Flow Diagram |  |



#### References



| Ref. # | Title | Version |

| --- | --- | --- |

| 1 | AUTOSAR Specification of Memory Mapping | v1.3.0 R4.0 Rev 2 |

| 2 | MDD Guideline | EA4 01.02.00 |

| 3 | EA4 Software Naming Conventions | 01.02.00 |

| 4 | Software Design and Coding Standards | 2.01 |

| 5 | FDD: CM200B_DmaCfgAndUse_Design | See Synergy subproject version |
