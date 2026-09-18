---
title: 'CM320A_Adc1CfgAndUse_Impl — Adc1CfgAndUse_IntegrationManual'
description: 'Converted Word (.docx) document Adc1CfgAndUse_IntegrationManual.docx from module CM320A_Adc1CfgAndUse_Impl.'
sidebar:
  hidden: true
---

> **Source:** `Adc1CfgAndUse_IntegrationManual.docx` (Word (.docx), 79 KB, in-module path `doc/`)
>
> Converted from OOXML (`word/document.xml`); headings, lists and tables preserved. Embedded objects and images are inventoried below.
>
> props: {'title': 'MDD Design Template V1.0', 'creator': 'Nexteer', 'subject': '', 'keywords': '', 'description': 'version 1.0 dated 24-Dec-2013'}; embedded images: 1 (png); OLE embeddings: 0; tables converted: 12

## Converted content

Integration Manual

For

Adc1 Cfg And Use

VERSION: 3.0

DATE: 09-Jun-2016

Prepared By:

Software Group,

Nexteer Automotive,

Saginaw, MI, USA

Location: The official version of this document is stored in the Nexteer Configuration Management System.

Revision History



| Sl. No. | Description | Author | Version | Date |

| --- | --- | --- | --- | --- |

| 1 | Initial version | Selva Sengottaiyan | 1.0 | 4-May-2015 |

| 2 | Updated for design rev. 2.0.0 | Rijvi | 2.0 | 05-Feb-2016 |

| 3 | Added Newperiodic and removed one server runnable | Avinash James | 3.0 | 9-Jun-2016 |



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

|  | <ADD more to the table if applicable> |



## References

This section lists the title & version of all the documents that are referred for development of this document



| Sr. No. | Title | Version |

| --- | --- | --- |

| 1 | FDD – CM320A Adc1CfgAndUse | See synergy sub project version |



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

Yes

### Da Vinci Parameter Configuration Changes



| Parameter | Notes | SWC |

| --- | --- | --- |

| Refer the . m file in the design |  |  |



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

Refer DataDict.m file

### Required Global Data Outputs

Refer DataDict.m file

### Specific Include Path present

Yes

## Runnable Scheduling

This section specifies the required runnable scheduling.



| Init | Scheduling Requirements | Trigger |

| --- | --- | --- |

| Adc1CfgAndUseInit1 | None | RTE |





| Runnable | Scheduling Requirements | Trigger |

| --- | --- | --- |

| Adc1CfgAndUsePer1 | None | 2ms(RTE) |

| Adc1CfgAndUsePer2 | None | 2ms(RTE) |

| Adc1CfgAndUseAdc1EnaCnvn_Oper | None | On event |



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

None
