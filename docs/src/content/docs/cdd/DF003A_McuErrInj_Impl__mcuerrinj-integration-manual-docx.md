---
title: 'DF003A_McuErrInj_Impl — McuErrInj Integration Manual'
description: 'Converted Word (.docx) document McuErrInj Integration Manual.docx from module DF003A_McuErrInj_Impl.'
sidebar:
  hidden: true
---

> **Source:** `McuErrInj Integration Manual.docx` (Word (.docx), 73 KB, in-module path `doc/`)
>
> Converted from OOXML (`word/document.xml`); headings, lists and tables preserved. Embedded objects and images are inventoried below.
>
> props: {'title': 'MDD Design Template V1.0', 'creator': 'Nexteer', 'subject': '', 'keywords': '', 'description': 'version 1.0 dated 24-Dec-2013'}; embedded images: 1 (png); OLE embeddings: 0; tables converted: 12

## Converted content

Integration Manual

For

McuErrInj

VERSION: 2.0

DATE: 24-Jul-2017

Prepared By:

Software Group,

Nexteer Automotive,

Saginaw, MI, USA

Location: The official version of this document is stored in the Nexteer Configuration Management System.

Revision History



| Sl. No. | Description | Author | Version | Date |

| --- | --- | --- | --- | --- |

| 1 | Initial version | Avinash James | 1.0 | 15-Mar-2017 |

| 2 | Update to include the tursted function | Avinash James | 2.0 | 24-Jul-2017 |



Table of Contents

1Abbrevations And Acronyms4

2References5

3Dependencies6

3.1SWCs6

3.2Global Functions(Non RTE) to be provided to Integration Project6

4Configuration REQUIREMeNTS7

4.1Build Time Config7

4.2Configuration Files to be provided by Integration Project7

4.3Da Vinci Parameter Configuration Changes7

4.4DaVinci Interrupt Configuration Changes7

4.5Manual Configuration Changes7

5Integration  DATAFLOW REQUIREMENTS8

5.1Required Global Data Inputs8

5.2Required Global Data Outputs8

5.3Specific Include Path present8

6Runnable Scheduling9

7Memory Map REQUIREMENTS10

7.1Mapping10

7.2Usage10

7.3NvM Blocks10

8Compiler Settings11

8.1Preprocessor MACRO11

8.2Optimization Settings11

9Appendix12

## Abbrevations And Acronyms



| Abbreviation | Description |

| --- | --- |

| DFD | Design functional diagram |

| MDD | Module design Document |

| FDD | Functional Design Document |



## References

This section lists the title & version of all the documents that are referred for development of this document



| Sr. No. | Title | Version |

| --- | --- | --- |

| 1 | FDD – DF003A McuDiagc | See Synergy subproject version |

| 2 | Software Naming Conventions | Process 04.04.02 |

| 3 | Software Coding Standards | Process 04.04.02 |



## Dependencies

### SWCs



| Module | Required Feature |

| --- | --- |

| None |  |



Note : Referencing the external components should be avoided in most cases. Only in unavoidable circumstance external components should be referred. Developer should track the references.

### Global Functions(Non RTE) to be provided to Integration Project

InjVrfyCritRegErr() – Function to Inject micro diagnostic error in Critical Registers

InjMcuVltgMonrErr() – Function to Inject micro diagnostic error in Core voltage monitor

InjClkMonrErr() – Function to Inject micro diagnostic error in Clock Monitors

InjOsTmpGenericRtErr () – Function to Inject Temporary Run time error in Operating System

InjOsPrmntGenericRtErr () – Function to Inject Permanent Run time error in Operating System

InjWdgErr () – Function to Watchdog errors

InjFpuErr ()  – Function to Inject floating point exceptions

InjMemProtnErr ()  – Function to Inject Memory protection errors

InjModErr () – Function to Inject mode errors

InjMcuRtErr () – Function to Inject Mcu Run Time errors

InjCodFlsEccErr() – Function to Inject Code flash ECC errors

InjRamMemErr( ) – Function to Inject peripheral and local RAM ECC errors

InjEcmMstChkrRtErr(void) () – Function to Inject micro diagnostic error in ECM Master and Slave

InjUkwnStrtUpDetdErr(void) -() – Function to Inject unknown startup

InjIpgRtErr(void) () – Function to Inject Run time IPG errors

InjRtPegErr(void) – Function to Inject Run time Peg errors

InjDataParErr() – Function to Inject Data Parity errors

InjDmaErr() – Function Dma errors

InjMcuDiagcErr() – Function to Inject loss ofmotor control ISR errors

InjAdcErr() – Function to Inject ADC errors

InjProgSeqErr () – Function to inject program sequence errors

InjPbgRtErr () - Function to inject PBG run time errors

InjSwFpuErr () – Function to inject software Floating point error

McuDiagcTestTrustd() – Trusted function call from OS

## Configuration REQUIREMeNTS

### Build Time Config



| Modules | Notes |  |

| --- | --- | --- |

| MCUDIAGCERRINJ | STD_OFF for other builds STD_ON for uDiag test builds |  |



### Configuration Files to be provided by Integration Project

None

### Da Vinci Parameter Configuration Changes



| Parameter | Notes | SWC |

| --- | --- | --- |

| None |  |  |



### DaVinci Interrupt Configuration Changes



| ISR Name | VIM # | Priority Dependency | Notes |

| --- | --- | --- | --- |

| None |  |  |  |



### Manual Configuration Changes



| Constant | Notes | SWC |

| --- | --- | --- |

| OS Memory protection has to be extended to include the reserved RAM & invalid memory area .Also execution from RAM need to be enabled too as per the settings below |  |  |



(osuint32)0x0100a000UL, /* MPU region 3 */

(osuint32)0x0100bffcUL,

(osuint32)0x03ff00edUL,

(osuint32)0x10020000UL, /* MPU region 4 */

(osuint32)0x10020848UL,

(osuint32)0x03ff00dbUL,

(osuint32)0xfb000000UL, /* MPU region 5 */

(osuint32)0xfebdfffcUL,

(osuint32)0x03ff00d9UL,

(osuint32) 0xF3000000UUL, /* MPU region 6 */

(osuint32) 0xF4000000UL,

(osuint32)0x03ff00dbUL,

(osuint32)&osGlobalShared_StartAddr, /* MPU region Global shared*/

(osuint32)&osGlobalShared_EndAddr,

(osuint32)0x03ff00fbUL,

## Integration  DATAFLOW REQUIREMENTS

### Required Global Data Inputs

Refer DataDict.m file

### Required Global Data Outputs

Refer DataDict.m file

### Specific Include Path present

Yes

## Runnable Scheduling

This section specifies the required runnable scheduling.



| Init | Scheduling Requirements | Trigger |

| --- | --- | --- |

| McuDiagcInit1 | None | RTE (Init) |





| Runnable | Scheduling Requirements | Trigger |

| --- | --- | --- |

| McuDiagcPer1 | None | RTE (2 ms) |

| ClrErrInjReg_Oper | None | On invocation |

| ReadErrInjReg_Oper | None | On invocation |

| StrtErrInjCntr_Oper | None | On invocation |

| UpdErrInjReg_Oper | None | On invocation |



## Memory Map REQUIREMENTS

### Mapping



| Memory Section | Contents | Notes |

| --- | --- | --- |

| McuErrInj_START_SEC_VAR_INIT_128 | Data section for DMA write |  |

| McuErrInjGlobalShared_START_SEC_VAR_CLEARED_32 | Global shared data access |  |



* Each …START_SEC… constant is terminated by a …STOP_SEC… constant as specified in the AUTOSAR Memory Mapping requirements.

### Usage



| Feature | RAM | ROM |

| --- | --- | --- |

| None |  |  |



Table 1: ARM Cortex R4 Memory Usage

### NvM Blocks

None

## Compiler Settings

### Preprocessor MACRO

None

### Optimization Settings

None

## Appendix

None
