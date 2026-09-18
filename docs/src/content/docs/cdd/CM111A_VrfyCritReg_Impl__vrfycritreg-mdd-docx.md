---
title: 'CM111A_VrfyCritReg_Impl — VrfyCritReg_MDD'
description: 'Converted Word (.docx) document VrfyCritReg_MDD.docx from module CM111A_VrfyCritReg_Impl.'
sidebar:
  hidden: true
---

> **Source:** `VrfyCritReg_MDD.docx` (Word (.docx), 94 KB, in-module path `doc/`)
>
> Converted from OOXML (`word/document.xml`); headings, lists and tables preserved. Embedded objects and images are inventoried below.
>
> props: {'title': 'Module Design Document', 'creator': 'Windows User', 'subject': '', 'keywords': '', 'description': ''}; embedded images: 3 (png); OLE embeddings: 0; tables converted: 11

## Converted content

For

VrfyCritReg

May 24, 2017

Prepared For:

Software Engineering

Nexteer Automotive,

Saginaw, MI, USA

Prepared By:

Selva Sengottaiyan

Nexteer Automotive,

Saginaw, MI, USAChange History



| Description | Author | Version | Date |

| --- | --- | --- | --- |

| Initial Version | Sankardu Varadapureddi | 1 | 14-Jan-2016 |

| Updated to “ Critical register” checks at init and periodic functions | Selva Sengottaiyan | 2 | 14-Apr-2016 |

| Updated to include support for MCAL write verify failures | Avinash James | 3 | 24-May-2017 |



Table of Contents

1Introduction5

1.1Purpose5

1.2Scope5

2VrfyCritReg High-Level Description6

3Design details of software module7

3.1Graphical representation of VrfyCritReg7

3.2Data Flow Diagram7

3.2.1Component level DFD7

3.2.2Function level DFD7

4Constant Data Dictionary8

4.1Program (fixed) Constants8

4.1.1Embedded Constants8

5Software Component Implementation9

5.1Sub-Module Functions9

5.1.1Init: VrfyCritRegInit19

5.1.1.1Design Rationale9

5.1.1.2Module Outputs9

5.1.2Per: VrfyCritRegPer19

5.1.2.1Design Rationale9

5.1.2.2Store Module Inputs to Local copies9

5.1.2.3(Processing of function)………9

5.1.2.4Store Local copy of outputs into Module Outputs9

5.2Server Runables9

5.3Interrupt Functions9

5.4Module Internal (Local) Functions9

5.4.1Local Function #29

5.4.1.1Description9

5.5GLOBAL Function/Macro Definitions10

6Known Limitations with Design11

7UNIT TEST CONSIDERATION12

Appendix AAbbreviations and Acronyms13

Appendix BGlossary14

Appendix CReferences15

## Introduction

### Purpose

### Scope

## VrfyCritReg High-Level Description

Refer to FDD

## Design details of software module

### Graphical representation of VrfyCritReg

### Data Flow Diagram

Refer FDD

#### Component level DFD

#### Function level DFD

## Constant Data Dictionary

### Program (fixed) Constants

#### Embedded Constants

Refer .m file

#### Local Constants



| Constant Name | Data Type | Value |

| --- | --- | --- |

| SYSCRITREGFLT_CNT_U08 | uint8 | 2 |

| CRITREGFLT_CNT_U08 | uint8 | 1 |

| NOFLT_CNT_U08 | uint8 | 0 |

| SHIFTBYBYTE_CNT_U08 | uint8 | 8 |

| VRFYCRITREGMCALFLT_CNT_U08 | uint8 | 4 |



## Software Component Implementation

### Sub-Module Functions

### Init: VrfyCritRegInit1

### Design Rationale

Refer FDD

### Module Outputs

None

### Per: VrfyCritRegPer1

### Design Rationale

Refer FDD

### Store Module Inputs to Local copies

None

### (Processing of function)………

Refer FDD

### Store Local copy of outputs into Module Outputs

None

### Per: VrfyCritRegPer2

### Design Rationale

Refer FDD

### Store Module Inputs to Local copies

None

### (Processing of function)………

Refer FDD

### Store Local copy of outputs into Module Outputs

None

### Server Runables: MCalReadVrfyFailFltInfo_Oper

### Design Rationale

Refer FDD

### Store Module Inputs to Local copies

None

### (Processing of function)………

Refer FDD

### Store Local copy of outputs into Module Outputs

None

### Interrupt Functions

None

### Module Internal (Local) Functions

### Local Function #1



| Function Name | SysCritReg<Register Short Name>IninChk | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | NA |  |  |  |

| Return Value | &SysRegsOk_Uls_T_lgc | boolean | FALSE | TRUE |



### Description

Set ' SysRegsOk_Uls_T_lgc to FALSE if CPU System Register values are not equal to expected values.  This is configured to be called from trusted function because it needs to run in supervisor mode

### Local Function #2



| Function Name | SysCritReg<Register Short Name>PerChk | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | NA |  |  |  |

| Return Value | &SysRegsOk_Uls_T_lgc | boolean | FALSE | TRUE |



### Description

Set ' SysRegsOk_Uls_T_lgc to FALSE if CPU System Register values are not equal to expected values.  This is configured to be called from trusted function because it needs to run in supervisor mode

### GLOBAL Function/Macro Definitions

### Global Function #1



| Function Name | CritRegPerChk | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | NA |  |  |  |

| Return Value | NtcParamInfo_Cnt_T_u08 | uint8 | 0U | 2U |



### Description

Set ' NtcParamInfo_Cnt_T_u08 to 1 if CPU Non System Register values are not equal to expected values. Set ' NtcParamInfo_Cnt_T_u08 to 2 if CPU System Register values are not equal to expected values. Set ' NtcParamInfo_Cnt_T_u08 to 0 if none of the above conditions are true.  This is configured as a trusted function because it needs to run in supervisor mode

### Global Function #2



| Function Name | CritRegInitChk | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | NA |  |  |  |

| Return Value | NtcParamInfo_Cnt_T_u08 | uint8 | 0U | 2U |



### Description

Set ' NtcParamInfo_Cnt_T_u08 to 1 if CPU Non System Register values are not equal to expected values. Set ' NtcParamInfo_Cnt_T_u08 to 2 if CPU System Register values are not equal to expected values. Set ' NtcParamInfo_Cnt_T_u08 to 0 if none of the above conditions are true.  This is configured as a trusted function because it needs to run in supervisor mode

### Global Function #3



| Function Name | SysCritRegIninChk | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | NA |  |  |  |

| Return Value | SysRegsOk_Uls_T_lgc | boolean | FALSE | TRUE |



### Description

Set ' SysRegsOk_Uls_T_lgc to FALSE if CPU System Register values are not equal to expected values.  This is configured to be called from trusted function because it needs to run in supervisor mode

### Global Function #4



| Function Name | SysCritRegPerChk | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | NA |  |  |  |

| Return Value | SysRegsOk_Uls_T_lgc | boolean | FALSE | TRUE |



### Description

Set ' SysRegsOk_Uls_T_lgc to FALSE if CPU System Register values are not equal to expected values.  This is configured to be called from trusted function because it needs to run in supervisor mode

## Known Limitations with Design

## UNIT TEST CONSIDERATION

None

#### Abbreviations and Acronyms



| Abbreviation or Acronym | Description |

| --- | --- |



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

| 1 | AUTOSAR Specification of Memory Mapping (Link:AUTOSAR_SWS_MemoryMapping.pdf) | v1.3.0 R4.0 Rev 2 |

| 2 | MDD Guideline | Software Engineering Process 04.04.02 |

| 3 | Software Naming Conventions.doc | Software Engineering Process 04.04.02 |

| 4 | Software Design and Coding Standards.doc | Software Engineering Process 04.04.02 |

| 5 | FDD : CM111A_VrfyCritReg_Design | See Synergy sub project version |
