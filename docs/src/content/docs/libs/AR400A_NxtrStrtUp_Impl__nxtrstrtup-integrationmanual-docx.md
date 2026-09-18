---
title: 'AR400A_NxtrStrtUp_Impl — NxtrStrtUp_IntegrationManual'
description: 'Converted Word (.docx) document NxtrStrtUp_IntegrationManual.docx from module AR400A_NxtrStrtUp_Impl.'
sidebar:
  hidden: true
---

> **Source:** `NxtrStrtUp_IntegrationManual.docx` (Word (.docx), 73 KB, in-module path `doc/`)
>
> Converted from OOXML (`word/document.xml`); headings, lists and tables preserved. Embedded objects and images are inventoried below.
>
> props: {'title': 'MDD Design Template V1.0', 'creator': 'Nexteer', 'subject': '', 'keywords': '', 'description': 'version 1.0 dated 24-Dec-2013'}; embedded images: 1 (png); OLE embeddings: 0; tables converted: 12

## Converted content

Integration Manual

For

NxtrStrtUp

VERSION: 1

DATE: 06/01/17

Prepared By:

Software Group,

Nexteer Automotive,

Saginaw, MI, USA

Location: The official version of this document is stored in the Nexteer Configuration Management System.

Revision History



| Sl. No. | Description | Author | Version | Date |

| --- | --- | --- | --- | --- |

| 1 | Initial version | Jared Julien | 1 | 06/01/17 |



Table of Contents

1Abbrevations And Acronyms4

2References5

3Dependencies6

3.1SWCs6

3.2Global Functions(Non RTE) to be provided to Integration Project6

4Configuration REQUIREMeNTS7

4.1Build Time Config7

4.2Configuration Files to be provided by Integration Project7

4.3DaVinci Parameter Configuration Changes7

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

|  | <ADD more to the table if applicable> |



## References

This section lists the title & version of all the documents that are referred for development of this document



| Sr. No. | Title | Version |

| --- | --- | --- |

| 1 | MDD Guidelines | Process 04.00.00 |

| 2 | Software Naming Conventions | Process 04.00.00 |

| 3 | Software Coding Standards | Process 04.00.00 |

| 4 | AR400A_NxtrStrtUp_Design | See Synergy subproject version |



## Dependencies

### SWCs



| Module | Required Feature |

| --- | --- |

| None | N/A |



Note : Referencing the external components should be avoided in most cases. Only in unavoidable circumstance external components should be referred. Developer should track the references.

### Global Functions(Non RTE) to be provided to Integration Project

None

## Configuration REQUIREMeNTS

### Build Time Config



| Modules | Notes |  |

| --- | --- | --- |

| None |  |  |



### Configuration Files to be provided by Integration Project

None

### DaVinci Parameter Configuration Changes



| Parameter | Notes | SWC |

| --- | --- | --- |

| N/A |  |  |



### DaVinci Interrupt Configuration Changes



| ISR Name | Interrupt Category (FE/EI) | Interrupt Channel Number | Priority Dependency | Notes |

| --- | --- | --- | --- | --- |

| N/A |  |  |  |  |



### Manual Configuration Changes



|  | Notes | SWC |

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

| N/A |  |  |





| Runnable | Scheduling Requirements | Trigger |

| --- | --- | --- |

| N/A |  |  |



.

## Memory Map REQUIREMENTS

### Mapping



| Memory Section | Contents | Notes |

| --- | --- | --- |

| .appstrtvect | Entry point to application | Must be placed at the location that the bootloader is expected to jump to via linker command file. |



* Each …START_SEC… constant is terminated by a …STOP_SEC… constant as specified in the AUTOSAR Memory Mapping requirements.

### Usage



| Feature | RAM | ROM |

| --- | --- | --- |

| N/A |  |  |



### NvM Blocks

None

## Compiler Settings

### Preprocessor MACRO

None

### Optimization Settings

The following option must be specified in the main .gpj project file:

-nostartfiles

This change prevents the use of the Green Hills startup library which this component replaces.

## Appendix

The following symbols need to be defined in the linker command file for the project surrounding RAM sections that are to be cleared at init.

These symbols are used by the library to denote the beginning and end of RAM that will be cleared during application init.  The intent is to keep the range as small as possible to optimize startup timing while including all RAM that is guaranteed to be cleared at init.  Due to the way Nexteer structures their memory map the cleared section may contain initialized sections (*data and *sdata) as well.  This will not cause any functional issues but will hinder performance slightly.

Caution: if a variable is outside of the range between these two symbols its value at init cannot be assured.  It is recommended that the .map file be analyzed once the changes have been integrated and the project compiles to ensure that there are no variables that fall outside of this range.
