---
title: 'AR099A_McalErrHndlg_Impl — McalErrHndlg_IntegrationManual'
description: 'Converted Word (.docx) document McalErrHndlg_IntegrationManual.docx from module AR099A_McalErrHndlg_Impl.'
sidebar:
  hidden: true
---

> **Source:** `McalErrHndlg_IntegrationManual.docx` (Word (.docx), 69 KB, in-module path `doc/`)
>
> Converted from OOXML (`word/document.xml`); headings, lists and tables preserved. Embedded objects and images are inventoried below.
>
> props: {'title': 'MDD Design Template V1.0', 'creator': 'Nexteer', 'subject': '', 'keywords': '', 'description': 'version 1.0 dated 24-Dec-2013'}; embedded images: 1 (png); OLE embeddings: 0; tables converted: 11

## Converted content

Integration Manual

For

McalErrHndlg

VERSION: 1

DATE: 5-30-2017

Prepared By:

Jared Julien,

Nexteer Automotive,

Saginaw, MI, USA

Location: The official version of this document is stored in the Nexteer Configuration Management System.

Revision History



| Sl. No. | Description | Author | Version | Date | Approved By |

| --- | --- | --- | --- | --- | --- |

| 1 | Initial version | J. Julien | 1.0 | - | - |



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

7.2NvM Blocks10

8Compiler Settings11

8.1Preprocessor MACRO11

8.2Optimization Settings11

9Appendix12

## Abbrevations And Acronyms



| Abbreviation | Description |

| --- | --- |

| DFD | Design functional diagram |

| MDD | Module design Document |

|  | <ADD more to the table if applicable> |



## References

This section lists the title & version of all the documents that are referred for development of this document



| Sr. No. | Title | Version |

| --- | --- | --- |

| 1 | MDD Guidelines | Process 04.00.00 |

| 2 | Software Naming Conventions | Process 04.00.00 |

| 3 | Software Coding Standards | Process 04.00.00 |

| 4 | AR099A_McalErrHndlg_Design | See Synergy subproject version |



## Dependencies

### SWCs



| Module | Required Feature |

| --- | --- |

| None | N/A |



Note : Referencing the external components should be avoided in most cases. Only in unavoidable circumstance external components should be referred. Developer should track the references.

### Global Functions(Non RTE) to be provided to Integration Project

HndlMcalWrVrfyErr

Fls_CallSwitchBFlashErrorNotification

HndlMcalDemErr

## Configuration REQUIREMeNTS

### Build Time Config



| Modules | Notes |  |

| --- | --- | --- |

| None |  |  |



### Configuration Files to be provided by Integration Project

### Da Vinci Parameter Configuration Changes



| Parameter | Value | SWC |

| --- | --- | --- |

| /Renesas/EcucDefs_Dio/Dio/DioGeneral/DioWriteVerifyErrorInterface | HndlMcalWrVrfyErr | Dio |

| /Renesas/EcucDefs_Fls/Fls/FlsGeneral/FlsWriteVerifyErrorInterface | HndlMcalWrVrfyErr | Fls |

| /Renesas/EcucDefs_Mcu/Mcu/McuGeneralConfiguration/McuWVErrorNotification | HndlMcalWrVrfyErr | Mcu |

| /Renesas/EcucDefs_Port/Port/PortGeneral/PortWriteVerifyErrorInterface | HndlMcalWrVrfyErr | Port |

| /Renesas/EcucDefs_Spi/Spi/SpiGeneral/SpiWriteVerifyErrorInterface | HndlMcalWrVrfyErr | Spi |

| /Renesas/DriverA/Wdg/WdgGeneral/WdgWriteVerifyErrorInterface | HndlMcalWrVrfyErr | Wdg |



### DaVinci Interrupt Configuration Changes



| ISR Name | VIM # | Priority Dependency | Notes |

| --- | --- | --- | --- |

| N/A |  |  |  |



### Manual Configuration Changes



| Constant | Notes | SWC |

| --- | --- | --- |

| N/A |  |  |



## Integration  DATAFLOW REQUIREMENTS

### Required Global Data Inputs

None

### Required Global Data Outputs

None

### Specific Include Path present

Yes

## Runnable Scheduling

This section specifies the required runnable scheduling.



| Init | Scheduling Requirements | Trigger |

| --- | --- | --- |

| McalErrHndlgInit1 | None | RTE |





| Runnable | Scheduling Requirements | Trigger |

| --- | --- | --- |

| McalErrHndlgPer1 | None | 10 ms |



.

## Memory Map REQUIREMENTS

### Mapping



| Memory Section | Contents | Notes |

| --- | --- | --- |

| McalErrHndlg_START_SEC_RAMCODE | Functions | Must be mapped to executable RAM* |



* Each …START_SEC… constant is terminated by a …STOP_SEC… constant as specified in the AUTOSAR Memory Mapping requirements.

*See Fls module integration manual for more information on setting up this special RAM section.

### NvM Blocks

*See DataDict.m

## Compiler Settings

### Preprocessor MACRO

None

### Optimization Settings

N/A

## Appendix

### Memory Mapping Changes for MCAL DEM error reporting redirect

The MemMap.h of the integration project needs to include some special definitions for capture the error reporting from the MCAL components Fls, Mcu, and Spi to the DEM.  This is accomplished by adding the following definition into the MemMap section definitions for the module.

#include "McalErrHndlg.h"

#define Dem_ReportErrorStatus HndlMcalDemErr

The sections into which the above definition must be placed are listed below:

MCU_START_SEC_PRIVATE_CODE

SPI_START_SEC_CODE_FAST

FLS_START_SEC_PRIVATE_CODE

And a corresponding undefine needs to be placed in the corresponding STOP sections as follows:

#undef Dem_ReportErrorStatus

In the following sections:

MCU_STOP_SEC_PRIVATE_CODE

SPI_STOP_SEC_CODE_FAST

FLS_STOP_SEC_PRIVATE_CODE
