---
title: 'ES104B_XcpIf_Impl — XcpIf_Integration_Manual'
description: 'Converted Word (.docx) document XcpIf_Integration_Manual.docx from module ES104B_XcpIf_Impl.'
sidebar:
  hidden: true
---

> **Source:** `XcpIf_Integration_Manual.docx` (Word (.docx), 82 KB, in-module path `doc/`)
>
> Converted from OOXML (`word/document.xml`); headings, lists and tables preserved. Embedded objects and images are inventoried below.
>
> props: {'title': 'MDD Design Template V1.0', 'creator': 'Nexteer', 'subject': '', 'keywords': '', 'description': 'version 1.0 dated 24-Dec-2013'}; embedded images: 1 (png); OLE embeddings: 0; tables converted: 12

## Converted content

Integration Manual

For

XCP Interfrace (XcpIf)

VERSION: 1.00

DATE: 19-Jan-2018

Prepared By:

ESG Software,

Nexteer Automotive,

Saginaw, MI, USA

Document Change History



| Version | Description | Author(s) | Revision Date | Approved By | Approved Date | Status |

| --- | --- | --- | --- | --- | --- | --- |

| 1.00 | Initial document release | K. Smith | 19-Jan-2018 | K. Smith | 19-Jan-2018 | Released |



Note:

This version 1.00 was baselined without requirements or a design finalized.

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

7.3Non  RTE NvM Blocks10

7.4RTE NvM Blocks10

8Compiler Settings11

8.1Preprocessor MACRO11

8.2Optimization Settings11

9Appendix12

## Abbrevations And Acronyms



| Abbreviation | Description |

| --- | --- |

| DFD | Design functional diagram |

| MDD | Module design Document |



## References

This section lists the title & version of all the documents that are referred for development of this document



| Sr. No. | Title | Version |

| --- | --- | --- |

| 1 | Software Naming Conventions | 1.02 |

| 2 | Software Design and Coding Standards | 2.01 |



## Dependencies

### SWCs



| Module | Required Feature |

| --- | --- |

| <Name of SWC> | <Addition of global data, function>*. |



Note : Referencing the external components should be avoided in most cases. Only in unavoidable circumstance external components should be referred. Developer should track the references.

### Global Functions(Non RTE) to be provided to Integration Project

The following functions need to be defined as non-trusted.

- CopyCalPageReq_Oper

- SetCalPageReq_Oper

- Xcp_Event

The following function needs to be defined as trusted:

- XcpAppl_CalibrationWriteTrustd

## Configuration REQUIREMeNTS

### Build Time Config



| Modules | Notes |  |

| --- | --- | --- |

| None |  |  |



### Configuration Files to be provided by Integration Project

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

| None |  |  |



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

| CDD_XcpIfInit1 | None | RTE (Init) |





| Runnable | Scheduling Requirements | Trigger |

| --- | --- | --- |

| CDD_XcpIfPer1 | None | RTE (100ms) |



.

## Memory Map REQUIREMENTS

### Mapping



| Memory Section | Contents | Notes |

| --- | --- | --- |

| None |  |  |



* Each …START_SEC… constant is terminated by a …STOP_SEC… constant as specified in the AUTOSAR Memory Mapping requirements.

### Usage



| Feature | RAM | ROM |

| --- | --- | --- |

| None |  |  |



Table 1: ARM Cortex R4 Memory Usage

### NvM Blocks

*See DataDict.m

## Compiler Settings

### Preprocessor MACRO

None

### Optimization Settings

None

## Appendix

### XCP Configuration

Below are the following options that need to be enabled for the component to properly work.

<< ADD XCP NOTES >>>

### XCP Configuration

Based on the XCP settings for the DAQ lists, components descriptions (arxml), source files (.c), and m-files are created based on the configuration. These compoents will also need to be imported into the project.

Key items

- DAQ runnables should be placed in the lowest priority task for a given runnable rate. This should be called before the checkpoint. This will ensure a good sample and avoid lag for a given runnable rate.

- Multiple DAQs can be configured to run at different rates. Each DAQ list will have its own set of description, source, and m-files to be integrated.

### Integration Compatibility with ES400A

If this component is used with ES400A version 2.0.0 or earlier will require a header file to be created to map constants that are defined in ES400A to the values used by ES104B. These values are different then where defined in ES104A. Below is a sample template that can be used:

File Name: CDD_XcpIf.h

File Contents:

## Template Change History
