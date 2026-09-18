---
title: 'CM101A_ExcpnHndlg_Impl — ExcpnHndlg Module Design Document'
description: 'Converted Word (.docx) document ExcpnHndlg Module Design Document.docx from module CM101A_ExcpnHndlg_Impl.'
sidebar:
  hidden: true
---

> **Source:** `ExcpnHndlg Module Design Document.docx` (Word (.docx), 98 KB, in-module path `doc/`)
>
> Converted from OOXML (`word/document.xml`); headings, lists and tables preserved. Embedded objects and images are inventoried below.
>
> props: {'title': 'Module Design Document', 'creator': 'Nexteer Employee', 'subject': '', 'keywords': '', 'description': ''}; embedded images: 2 (png); OLE embeddings: 0; tables converted: 2

## Converted content

For

ExcpnHndlg

04-Apr-2018

Prepared By:

Shruthi Raghavan,

Nexteer Automotive,

Saginaw, MI, USAChange History



| Description | Author | Version | Date |

| --- | --- | --- | --- |

| Initial Version | Avinash James | 1.0 | 05-Apr-2016 |

| Updated the #define for ECC single bit code flash fault | Avinash James | 2.0 | 18-Apr-2016 |

| Updated for v3.2.0 of the FDD | Selva Sengottaiyan | 3.0 | 24-June-2016 |

| Updated for v4.0.0 of the FDD | Avinash James | 4.0 | 17-Aug-2016 |

| Updated to remove constants that were used for parameter byte for CVM startup tests because this test is removed from CM101A | Shruthi Raghavan | 5.0 | 18-May-2017 |

| Added constants for the handling of code flash register write MCAL failure. | Shruthi Raghavan | 6.0 | 25-May-2017 |

| Removed the ProcEcmRst Function | Avinash James | 7.0 | 25-Jul-2017 |

| Added local constants | Avinash James | 8.0 | 21-Sep-2017 |

| Added handler for DTS single bit ECC error | Avinash James | 9.0 | 04-Apr-2018 |



Table of Contents1Introduction7

1.1Purpose7

2ExcpnHndlg & High-Level Description8

3Design details of software module9

3.1Graphical representation of ExcpnHndlg9

3.2Data Flow Diagram9

3.2.1Component level DFD9

3.2.2Function level DFD9

4Constant Data Dictionary10

4.1Program (fixed) Constants10

4.1.1Embedded Constants10

5Software Component Implementation14

5.1Sub-Module Functions14

5.1.1Init: ExcpnHndlgInit114

5.1.1.1Design Rationale14

5.1.1.2Module Outputs14

5.1.2Init: ExcpnHndlgInit214

5.1.2.1Design Rationale14

5.1.2.2Module Outputs14

5.1.3Per: ExcpnHndlgPer114

5.1.3.1Design Rationale14

5.1.3.2Store Module Inputs to Local copies14

5.1.3.3(Processing of function)………14

5.1.3.4Store Local copy of outputs into Module Outputs14

5.2Server Runables14

5.2.1ChkForStrtUpTest14

5.2.1.1Design Rationale14

5.2.1.2(Processing of function)………14

5.2.2FeNmiClkMonr0RtLowrLimFlt15

5.2.2.1Design Rationale15

5.2.2.2(Processing of function)………15

5.2.3FeNmiClkMonr0RtUpprLimFlt15

5.2.3.1Design Rationale15

5.2.3.2(Processing of function)………15

5.2.4FeNmiClkMonr1RtLowrLimFlt15

5.2.4.1Design Rationale15

5.2.4.2(Processing of function)………15

5.2.5FeNmiClkMonr1RtUpprLimFlt15

5.2.5.1Design Rationale15

5.2.5.2(Processing of function)………15

5.2.6FeNmiClkMonr2RtLowrLimFlt15

5.2.6.1Design Rationale15

5.2.6.2(Processing of function)………15

5.2.7FeNmiClkMonr2RtUpprLimFlt15

5.2.7.1Design Rationale15

5.2.7.2(Processing of function)………16

5.2.8FeNmiClkMonr3RtLowrLimFlt16

5.2.8.1Design Rationale16

5.2.8.2(Processing of function)………16

5.2.9FeNmiClkMonr3RtUpprLimFlt16

5.2.9.1Design Rationale16

5.2.9.2(Processing of function)………16

5.2.10FeNmiDmaTrf16

5.2.10.1Design Rationale16

5.2.10.2(Processing of function)………16

5.2.11FeNmiDmaRegAcsProtnErr16

5.2.11.1Design Rationale16

5.2.11.2(Processing of function)………16

5.2.12FeNmiEcmMstChkrCmp16

5.2.12.1Design Rationale16

5.2.12.2(Processing of function)………16

5.2.13FeNmiOperModErrFlsProgmModStrtd17

5.2.13.1Design Rationale17

5.2.13.2(Processing of function)………17

5.2.14FeNmiOperModErrSngChipInactv17

5.2.14.1Design Rationale17

5.2.14.2(Processing of function)………17

5.2.15FeNmiOperModErrTestModStrtd17

5.2.15.1Design Rationale17

5.2.15.2(Processing of function)………17

5.2.16FeNmiPeg17

5.2.16.1Design Rationale17

5.2.16.2(Processing of function)………17

5.2.17FeNmiWdg17

5.2.17.1Design Rationale17

5.2.17.2(Processing of function)………17

5.2.18GetMcuDiagcIdnData18

5.2.18.1Design Rationale18

5.2.18.2(Processing of function)………18

5.2.19ProcMpuExcpnErr18

5.2.19.1Design Rationale18

5.2.19.2(Processing of function)………18

5.2.20ProcNonCritOsErr18

5.2.20.1Design Rationale18

5.2.20.2(Processing of function)………18

5.2.21ProcPrmntOsErr18

5.2.21.1Design Rationale18

5.2.21.2(Processing of function)………18

5.2.22ProcPrvlgdInstrExcpnErr18

5.2.22.1Design Rationale18

5.2.22.2(Processing of function)………18

5.2.23ProcUkwnExcpnErr19

5.2.23.1Design Rationale19

5.2.23.2(Processing of function)………19

5.2.24SetMcuDiagcIdnData19

5.2.24.1Design Rationale19

5.2.24.2(Processing of function)………19

5.3Interrupt Functions19

5.3.1AlgnErrIrq19

5.3.1.1Design Rationale19

5.3.1.2(Processing of the ISR function)…..19

5.3.2FpuErrIrq19

5.3.2.1Design Rationale19

5.3.2.2(Processing of the ISR function)…..19

5.3.3SysErrIrq19

5.3.3.1Design Rationale19

5.3.3.2(Processing of the ISR function)…..19

5.3.4ResdOperIrq20

5.3.4.1Design Rationale20

5.3.4.2(Processing of the ISR function)…..20

5.4Module Internal (Local) Functions20

5.4.1ProcStrtUpOrSwRst20

5.4.1.1Design Rationale20

5.4.1.2Processing20

5.4.2ProcPinRst20

5.4.2.1Design Rationale20

5.4.2.2Processing20

5.4.3McuDiagcRstChk20

5.4.3.1Design Rationale21

5.4.3.2Processing21

5.5GLOBAL Function/Macro Definitions21

5.5.1GLOBAL Function #121

5.5.1.1Design Rationale21

5.5.1.2processing21

6Known Limitations with Design22

7UNIT TEST CONSIDERATION23

Appendix AAbbreviations and Acronyms24

Appendix BGlossary25

Appendix CReferences26

## Introduction

### Purpose

This document details the design in the FDD and also lists out any deviations which were made from the design for the implementation due to any constraints in development. ExcpnHndlg MDD describes the exception handling / reset cause determination for microcontroller diagnostics

## ExcpnHndlg & High-Level Description

Refer FDD

## Design details of software module

### Graphical representation of ExcpnHndlg

### Data Flow Diagram

#### Component level DFD

N/A

#### Function level DFD

N/A

## Constant Data Dictionary

### Program (fixed) Constants

#### Embedded Constants

#### Local Constants



| Constant Name | Resolution | Units | Value |

| --- | --- | --- | --- |

| FPCFGININVAL_CNT_T_U32 | 1 | Counts | 0x0000001CU |

| FPCFGREGID_CNT_S32 | 1 | Counts | 10 |

| FPCFGSELNID_CNT_S32 | 1 | Counts | 0 |

| FPUINVLDOPERSTSBIT_CNT_U32 | 1 | Counts | ((uint32)(0x00004000U)) |

| FPUDIVBYZEROSTSBIT_CNT_U32 | 1 | Counts | ((uint32)(0x00002000U)) |

| FPUOVFSTSBIT_CNT_U32 | 1 | Counts | ((uint32)(0x00001000U)) |

| MEMERRINFOREADWRBIT_CNT_U32 | 1 | Counts | ((uint32)(0x00000001U)) |

| CF1STERSTRADRPARMASK_CNT_U32 | 1 | Counts | ((uint32)(0x00000004U)) |

| CF1STERSTRDBLBITMASK_CNT_U32 | 1 | Counts | ((uint32)(0x00000002U)) |

| CF1STERSTRSNGBITMASK_CNT_U32 | 1 | Counts | ((uint32)(0x00000001U)) |

| PRPHLBUSDATAPARMASK_CNT_U32 | 1 | Counts | ((uint32)(0x10000000U)) |

| DTSDBLBITMASK_CNT_U32 | 1 | Counts | ((uint32)(0x80000000U)) |

| CODFLSSNGBITHARDFLT_CNT_U08 | 1 | Counts | 1U |

| CODFLSECCDBLBIT_CNT_U08 | 1 | Counts | 2U |

| CODFLSADRPAR_CNT_U08 | 1 | Counts | 4U |

| CODFLASHEXECENAREGFAILR_CNT_U08 | 1 | Counts | 8U |

| MEMBISTSTRTUPTESTFAILR_CNT_U08 | 1 | Counts | 1U |

| LCLRAMECCSNGBITHARDFLT_CNT_U08 | 1 | Counts | 1U |

| LCLRAMECCDBLBIT_CNT_U08 | 1 | Counts | 2U |

| INVLDRAMAREA_CNT_U08 | 1 | Counts | 4U |

| DTSDBLBIT_CNT_U08 | 1 | Counts | 2U |

| DTSSNGBITFLT_CNT_U08 | 1 | Counts | 4U |

| SPI0PRPHLRAMDBLBIT_CNT_U08 | 1 | Counts | 2U |

| SPI1PRPHLRAMDBLBIT_CNT_U08 | 1 | Counts | 2U |



## Software Component Implementation

### Sub-Module Functions

### Init: ExcpnHndlgInit1

### Design Rationale

Non-RTE function because it needs to be called before the OS is started - so that floating point exceptions can be enabled before anything uses floating point

### Module Outputs

None

### Init: ExcpnHndlgInit2

### Design Rationale

RTE function to initialize all the NTCs to pass

### Module Outputs

None

### Per: ExcpnHndlgPer1

### Design Rationale

RTE Periodic function called every 2 ms to check for OS errors

### Store Module Inputs to Local copies

Refer MDD

### (Processing of function)………

Triggered on Timing Event every 2ms

### Store Local copy of outputs into Module Outputs

None

### Server Runables

### ChkForStrtUpTest

### Design Rationale

Refer FDD

### (Processing of function)………

Refer FDD

### FeNmiClkMonr0RtLowrLimFlt

### Design Rationale

Refer FDD

### (Processing of function)………

R

*Body truncated: document is longer than the excerpt shown here.*
