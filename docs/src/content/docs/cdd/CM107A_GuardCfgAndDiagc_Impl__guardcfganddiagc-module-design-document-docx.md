---
title: 'CM107A_GuardCfgAndDiagc_Impl — GuardCfgAndDiagc Module Design Document'
description: 'Converted Word (.docx) document GuardCfgAndDiagc Module Design Document.docx from module CM107A_GuardCfgAndDiagc_Impl.'
sidebar:
  hidden: true
---

> **Source:** `GuardCfgAndDiagc Module Design Document.docx` (Word (.docx), 95 KB, in-module path `doc/`)
>
> Converted from OOXML (`word/document.xml`); headings, lists and tables preserved. Embedded objects and images are inventoried below.
>
> props: {'title': 'Module Design Document', 'creator': 'Windows User', 'subject': '', 'keywords': '', 'description': ''}; embedded images: 2 (jpg, png); OLE embeddings: 0; tables converted: 10

## Converted content

For

GuardCfgAndDiagc

Apr 10 , 2018

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

| Initial Version | Avinash James | 1.0 | 02/16/16 |

| Updates for PBG Register Lock bits and Syncm inclusion | Avinash James | 2.0 | 03/31/16 |

| Updates for design limitation | Avinash James | 3.0 | 04/10/18 |



Table of Contents

1Introduction5

1.1Purpose5

1.2Scope5

2GuardCfgAndDiagc & High-Level Description6

3Design details of software module7

3.1Graphical representation of GuardCfgAndDiagc7

3.2Data Flow Diagram7

3.2.1Component level DFD7

3.2.2Function level DFD7

4Constant Data Dictionary8

4.1Program (fixed) Constants8

4.1.1Embedded Constants8

5Software Component Implementation9

5.1Sub-Module Functions9

5.1.1Init: GuardCfgAndDiagcInit19

5.1.1.1Design Rationale9

5.1.1.2Module Outputs9

5.1.2Init: GuardCfgAndDiagcInit29

5.1.2.1Design Rationale9

5.1.2.2Module Outputs9

5.1.3Init: GuardCfgAndDiagcInit39

5.1.3.1Design Rationale9

5.1.3.2Module Outputs9

5.1.4Per: None9

5.2Server Runables9

5.3Interrupt Functions9

5.4Module Internal (Local) Functions10

5.4.1ConfigureFilterN10

5.4.1.1Design Rationale10

5.4.1.2Processing10

5.4.2ChkForPBGErr10

5.4.2.1Design Rationale10

5.4.2.2Processing10

5.4.3ChkForECMErr10

5.4.3.1Design Rationale10

5.4.3.2Processing11

5.4.4Vrfy32BitPBGRegAcs11

5.4.4.1Design Rationale11

5.4.4.2Processing11

5.4.5Vrfy16BitPBGRegAcs11

5.4.5.1Design Rationale11

5.4.5.2Processing11

5.4.6Vrfy8BitPBGRegAcs11

5.4.6.1Design Rationale11

5.4.6.2Processing11

5.5GLOBAL Function/Macro Definitions12

5.5.1GLOBAL Function #112

5.5.1.1Design Rationale12

5.5.1.2Processing12

6Known Limitations with Design13

7UNIT TEST CONSIDERATION14

Appendix AAbbreviations and Acronyms15

Appendix BGlossary16

Appendix CReferences17

## Introduction

### Purpose

### Scope

The following definitions are used throughout this document:

Shall: indicates a mandatory requirement without exception in compliance.

Should: indicates a mandatory requirement; exceptions allowed only with documented justification.

May: indicates an optional action.

## GuardCfgAndDiagc & High-Level Description

See FDD

## Design details of software module

### Graphical representation of GuardCfgAndDiagc

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

| PBGPROTNCMN_CNT_U32 | 1 | uint32 | 0x0405FE1FU |

| PBGUSRMODENA_CNT_U32 | 1 | uint32 | 0x02000000U |

| PBGUSRMODDI_CNT_U32 | 1 | uint32 | 0x00000000U |

| PBGSPID321ENA_CNT_U32 | 1 | uint32 | 0x000001C0U |

| PBGSPID31ENA_CNT_U32 | 1 | uint32 | 0x00000140U |

| PBGSPID21ENA_CNT_U32 | 1 | uint32 | 0x000000C0U |

| PBGSPID1ENA_CNT_U32 | 1 | uint32 | 0x00000040U |

| PBGSETNOREADWRACS_CNT_U32 | 1 | uint32 | 0x405FE5CU |

| NROF8BITREG_CNT_U08 | 1 | uint8 | ((uint8)0x09) |

| NROF32BITREG_CNT_U08 | 1 | uint8 | ((uint8)0x02) |

| READERRBIT_CNT_U32 | 1 | uint32 | ((uint32)1U<<6U) |

| WRERRBIT_CNT_U32 | 1 | uint32 | ((uint32)1U<<7U) |

| CFGERRBIT_CNT_U32 | 1 | uint32 | ((uint32)1U<<8U) |

| PBGERRBIT_CNT_U32 | 1 | uint32 | ((uint32)1U<<9U) |

| ECMERRBIT_CNT_U32 | 1 | uint32 | ((uint32)1U<<10U) |

| REGTYPE8BIT_CNT_U32 | 1 | uint32 | ((uint32)0U<<4U) |

| REGTYPE16BIT_CNT_U32 | 1 | uint32 | ((uint32)1U<<4U) |

| REGTYPE32BIT_CNT_U32 | 1 | uint32 | ((uint32)2U<<4U) |

| PBGSTRTUPTESTNOFAILR_CNT_U32 | 1 | uint32 | 0x0U |

| PBGPROTNLOCKENA_CNT_U32 | 1 | uint32 | 0x80000000U |



## Software Component Implementation

### Sub-Module Functions

#### Init: GuardCfgAndDiagcInit1

### Design Rationale

Non-RTE function for Guard configuration initialization of PEG, IPG, and PBG so that guard protection can be initialized and enabled before the RTE is started

### Module Outputs

Configuration registers for PEG, IPG, and PBG

#### Init: GuardCfgAndDiagcInit2

### Design Rationale

RTE Empty function for purposes of memory mapping

See FDD for more.

### Module Outputs

None

#### Init: GuardCfgAndDiagcInit3

### Design Rationale

Non-RTE function for Start Up Initialization test of PBG of Group 3A

See FDD for more.

### Module Outputs

None

### Per: None

### Server Runables

None

### Interrupt Functions

None

### Module Internal (Local) Functions

#### ConfigureFilterN



| Function Name | ConfigureFilterN | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | PbgProtReg | volatile uint32* | 0 | 0xFFFFFFFF |

|  | Val | uint32 | 0 | 0xFFFFFFFF |

|  | PbgStrtUpTestFailSts | Uint32 * | 0 | 0xFFFFFFFF |

| Return Value | None |  |  |  |



### Design Rationale

This local function sets the value Val to the register address PbgProtReg passed as the arguments and verifies the write operation was successful. If not a diagnostic is set.

### Processing

Figure 4.5.3 from SAN ver 1.20

#### ChkForPBGErr



| Function Name | ChkForPBGErr | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | PbgStrtUpTestFailSts | Uint32 * | 0 | 0xFFFFFFFF |

| Return Value | None |  |  |  |



### Design Rationale

This local function checks PBG access violation error is captured. If not set diagnostic, clear the error and if the error doesn’t clear set diagnostic.

### Processing

Figure 4.5.3 from SAN ver 1.20

#### ChkForECMErr



| Function Name | ChkForECMErr | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | PbgStrtUpTestFailSts | Uint32 * | 0 | 0xFFFFFFFF |

| Return Value | None |  |  |  |



### Design Rationale

This local function checkscwhether ECM captures the error sets diagnostic message and clears the ECM errors after the check else set diagnostic.

### Processing

Refer FDD 4.5.3 Implementation

#### Vrfy32BitPBGRegAcs



| Function Name | Vrfy32BitPBGRegAcs | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | PbgStrtUpTestFailSts | Uint32 * | 0 | 0xFFFFFFFF |

| Return Value | None |  |  |  |



### Design Rationale

This is defined to reduce the path count and modularizes the check for the 32 bit Access registers alone.

### Processing

#### Vrfy16BitPBGRegAcs



| Function Name | Vrfy16BitPBGRegAcs | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | PbgStrtUpTestFailSts | Uint32 * | 0 | 0xFFFFFFFF |

| Return Value | None |  |  |  |



### Design Rationale

This is defined to reduce the path count and modularizes the check for the 16 bit Access registers alone.

### Processing

#### Vrfy8BitPBGRegAcs



| Function Name | Vrfy8BitPBGRegAcs | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | PbgStrtUpTestFailSts | Uint32 * | 0 | 0xFFFFFFFF |

| Return Value | None |  |  |  |



### Design Rationale

This is defined to reduce the path count and modularizes the check for the 8 bit Access registers alone.

### Processing

### GLOBAL Function/Macro Definitions

### GLOBAL Function #1



| Function Name |  | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed |  |  |  |  |

| Return Value |  |  |  |  |



### Design Rationale

### Processing

## Known Limitations with Design

In the design for the error injection code, the reads make use of variables mapped in the global shared memory. Since we already have global variables mapped to global shared memory in the error injection code which are of type uint32, an explicit cast of uint32 is done for registers that are not unit32.Also the error injection code accesses register in the sys_regs.h file which is not currently included in the DF003A. This is being conditionally included in the component c file as this will not be part of the production code.

## UNIT TEST CONSIDERATION

None

#### Abbreviations and Acronyms



| A

*Body truncated: document is longer than the excerpt shown here.*
