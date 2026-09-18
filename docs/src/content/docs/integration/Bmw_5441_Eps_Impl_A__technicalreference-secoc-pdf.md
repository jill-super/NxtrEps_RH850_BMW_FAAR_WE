---
title: '_Bmw_5441_Eps_Impl_A — TechnicalReference_SecOC'
description: 'Converted PDF document TechnicalReference_SecOC.pdf from module _Bmw_5441_Eps_Impl_A.'
sidebar:
  hidden: true
---

> **Source:** `TechnicalReference_SecOC.pdf` (PDF, 644 KB, in-module path `doc/`)
>
> Converted from PDF with text extraction; layout, vector diagrams and scanned figures are not preserved. See the source PDF in the repository for the authoritative content.
>
> pages: 34; title: MICROSAR Secure Onboard Communication; author: Heiko Hübler, Markus Bart, Gunnar Meiss

## Converted content

### Page 1

MICROSAR Secure Onboard 
Communication 
Technical Reference 
 
 
Version 3.0.0 
 
 
 
 
 
 
 
 
 
 
 
Authors Heiko Hübler, Markus Bart, Gunnar Meiss 
Status Released

### Page 2

Technical Reference MICROSAR Secure Onboard Communication 
© 2017 Vector Informatik GmbH Version 3.0.0 2 
based on template version 5.9.0 
Document Information 
History 
Author Date Version Remarks 
Heiko Hübler 2014-10-02 1.00.00 ESCAN00078719: AR4-667: 
CONC_607_SecureOnboardCommunicati
on 
Heiko Hübler 2015-07-20 1.01.00 ESCAN00084099: FEAT-1475: SecOC-
Extensions, TP , CSM and encryption 
Gunnar Meiss 2016-02-25 1.02.00 ESCAN00088549: FEAT-1631: Trigger 
Transmit API with SduLength In/Out 
according to ASR4.2.2 
Heiko Hübler 2016-11-11 1.03.00 FEATC-379: SecOC Release 
Gunnar Meiss 2017-02-27 2.00.00 FEATC-852: FEAT-2365: Support 
standalone distribution of AR4.3 SecOC 
Heiko Hübler 2017-03-13 2.01.00 ESCAN00094184: BETA version - the 
BSW module is in BETA state 
Heiko Hübler 2017-07-26 3.00.00 STORYC-919: Development Mode 
Reference Documents 
No. Source Title Version 
[1] AUTOSAR AUTOSAR_SWS_SecureOnboardCommunication.pdf V4.3.0 
[2] AUTOSAR AUTOSAR_SWS_DET.pdf V4.3.0 
[3] AUTOSAR AUTOSAR_BasicSoftwareModules.pdf V1.0.0 
 
 
 
 
Caution 
We have configured the programs in accordance with your specifications in the 
questionnaire. Whereas the programs do support other configurations than the one 
specified in your questionnaire, Vector´s release of the programs delivered to your 
company is expressly restricted to the configuration you have specified in the 
questionnaire.

### Page 3

Technical Reference MICROSAR Secure Onboard Communication 
© 2017 Vector Informatik GmbH Version 3.0.0 3 
based on template version 5.9.0 
Contents 
1 Component History ................................ ................................ ................................ ...... 6 
2 Introduction................................ ................................ ................................ ................... 7 
2.1 Architecture Overview ................................ ................................ ........................ 7 
3 Functional Description ................................ ................................ ................................ . 8 
3.1 Features ................................ ................................ ................................ ............ 8 
3.1.1 Deviations ................................ ................................ .......................... 8 
3.1.2 Secured PDUs ................................ ................................ ................... 8 
3.1.2.1 Reception of Secured PDUs ................................ ............ 9 
3.1.2.2 Transmission of Secured PDUs ................................ ....... 9 
3.1.2.3 Secured PDU Collections................................ ................. 9 
3.1.3 Generic Freshness value interface ................................ ..................... 9 
3.2 Development Mode ................................ ................................ .......................... 10 
3.3 Initialization ................................ ................................ ................................ ...... 10 
3.4 Main Functions ................................ ................................ ................................ 10 
3.5 Error Handling ................................ ....................

### Page 4

Technical Reference MICROSAR Secure Onboard Communication 
© 2017 Vector Informatik GmbH Version 3.0.0 4 
based on template version 5.9.0 
5.3.2 SecOC_TxConfirmation ................................ ................................ ... 20 
5.3.3 SecOC_TriggerTransmit................................ ................................ ... 21 
5.3.4 SecOC_TpRxIndication ................................ ................................ .... 21 
5.3.5 SecOC_TpTxConfirmation ................................ ............................... 22 
5.3.6 SecOC_CopyRxData ................................ ................................ ....... 22 
5.3.7 SecOC_CopyTxData ................................ ................................ ........ 23 
5.3.8 SecOC_StartOfReception ................................ ................................ 24 
5.4 Configurable Interfaces ................................ ................................ .................... 24 
5.4.1 Notifications ................................ ................................ ..................... 24 
5.4.2 Callout Functions ................................ ................................ ............. 24 
5.4.2.1 SecOC_VerificationStatusCallout ................................ ... 25 
5.4.2.2 SecOC_GetTxFreshnessTruncData ............................... 25 
5.4.2.3 SecOC_GetTxFreshness ................................ ............... 26 
5.4.2.4 SecOC_SPduTxConfirmation ................................ ........ 27 
5.4.2.5 SecOC_GetRxFreshnessAuthData ................................ 27 
5.4.2.6 SecOC_GetRxFreshness................................ ............... 28 
5.5 Service Ports ................................ ................................ ................................ ... 30 
5.5.1 Client Server In

### Page 5

Technical Reference MICROSAR Secure Onboard Communication 
© 2017 Vector Informatik GmbH Version 3.0.0 5 
based on template version 5.9.0 
Illustrations 
Figure 2-1 AUTOSAR 4.3 Architecture Overview ................................ ......................... 7 
 
Tables 
Table 1-1 Component history................................ ................................ ...................... 6 
Table 3-1 Supported AUTOSAR standard conform features ................................ ....... 8 
Table 3-2 Not supported AUTOSAR standard conform features ................................ . 8 
Table 3-3 Service IDs ................................ ................................ ............................... 11 
Table 3-4 Errors reported to DET ................................ ................................ ............. 11 
Table 4-1 Static files ................................ ................................ ................................ . 12 
Table 4-2 Generated files ................................ ................................ ......................... 13 
Table 5-1 SecOC_InitMemory ................................ ................................ .................. 15 
Table 5-2 SecOC_Init ................................ ................................ ............................... 15 
Table 5-3 SecOC_DeInit ................................ ................................ ........................... 16 
Table 5-4 SecOC_GetVersionInfo ................................ ................................ ............ 16 
Table 5-5 SecOC_Transmit ................................ ................................ ...................... 17 
Table 5-6 SecOC_VerifyStatusOverride ................................ ................................ ... 18 
Table 5-6 SecOC_SetDev

### Page 6

Technical Reference MICROSAR Secure Onboard Communication 
© 2017 Vector Informatik GmbH Version 3.0.0 6 
based on template version 5.9.0 
1 Component History 
The component history gives an overv iew over the important milestones that are 
supported in the different versions of the component. 
Component Version New Features 
1.00.00 > Authentication of interface PDUs 
> Verification of interface PDUs 
2.00.00 > Support of lower layer Tp interface 
> Support of CSM 4.2 
3.01.00 > Trigger Transmit API with SduLength as in/out parameter 
4.00.00 > Generic Freshness value interface 
> Verification status override api 
5.00.00 > QM release 
> Support of splitting a Secured Message into an Authentic and an 
Cryptographic PDU 
> Support of Autosar 4.3 CSM 
> Post Build Loadable and Post Build Selectable 
6.00.00 > Support standalone distribution of AR4.3 SecOC 
7.01.00 > Removed support of CAL and CSM 4.2 
> Removed SecOC internal Freshness Co

*Excerpt: first 8 of 34 pages shown.*
