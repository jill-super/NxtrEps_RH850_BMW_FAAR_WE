---
title: 'Com — TechnicalReference_Com'
description: 'Converted PDF document TechnicalReference_Com.pdf from module Com.'
sidebar:
  hidden: true
---

> **Source:** `TechnicalReference_Com.pdf` (PDF, 1265 KB, in-module path `doc/`)
>
> Converted from PDF with text extraction; layout, vector diagrams and scanned figures are not preserved. See the source PDF in the repository for the authoritative content.
>
> pages: 85; title: MICROSAR COM; author: Dominik Biber, Safiulla Shakir, Gunnar Meiss, Heiko Hübler, Markus Bart, Anant Gupta, Büsra Bayrak

## Converted content

### Page 1

MICROSAR COM 
Technical Reference 
 
CFG5 
Version 6.03.00 
 
 
 
 
 
 
 
 
 
 
 
 
Authors Dominik Biber, Safiulla Shakir, Gunnar Meiss, Heiko 
Hübler, Markus Bart, Anant Gupta, Büsra Bayrak 
Status Released

### Page 2

Technical Reference MICROSAR COM 
© 2017 Vector Informatik GmbH Version 6.03.00 2 
based on template version 5.6.0 
Document Information 
History 
Author Date Version Remarks 
Safiulla Shakir 
Dominik Biber 
2012-02-21 1.00.00 > Adapted to Cfg5 
Dominik Biber 2012-07-19 2.00.00 > Adapted to AUTOSAR 4.0.3 
(ESCAN00058304) 
Dominik Biber 2012-12-11 2.01.00 > Added new feature descriptions 
> Invalidation Mechanism 
(ESCAN00061795) 
> Signal Reception Filtering 
(ESCAN00061805) 
> Signal Status Information 
(ESCAN00061799) 
Gunnar Meiss 2013-04-04 2.02.00 > AR4-325: Post-Build Loadable 
(ESCAN00064360) 
Dominik Biber 2013-04-12 2.02.00 > Added new feature Signal Gateway 
(ESCAN00064081) 
Adapted 
> Critical Sections (ESCAN00065327) 
Dominik Biber 2013-06-20 3.00.00 > Changed prototype description of 
Callout Functions (ESCAN00068096) 
Dominik Biber 2013-09-03 3.00.00 > Transmission Deadline Monitoring 
(ESCAN00070185) 
> Clarified transmission context of signals 
and signal groups (ESCAN00070200) 
> Updated limitations of Callout Functions 
(ESCAN00067146) 
> Support (ESCAN00070186) 
> Added support for 0-Bit signals 
(ESCAN00069728) 
Heiko Hübler 2013-09-23 3.00.00 > Added following API descriptions 
(ESCAN00070449): 
> Com_TpTxConfirmation 
> Com_CopyTxData 
> Com_TpRxIndication 
> Com_StartOfReception 
> Com_CopyRxData 
> Com_SendDynSignal 
> Com_ReceiveDynSignal 
Heiko Hübler 2013-10-02 3.00.00 > Added Chapter Large I-PDUs and 
Dynamic length signals

### Page 3

Technical Reference MICROSAR COM 
© 2017 Vector Informatik GmbH Version 6.03.00 3 
based on template version 5.6.0 
(ESCAN00070449) 
Heiko Hübler 2014-03-25 3.01.00 > Updated Com_ StartOfReception API 
according to ASR4.1.2 
(ESCAN00071922) 
Heiko Hübler 2014-04-16 3.01.00 > ESCAN00075083: AR4-710: Support 
IPDUGroup relevant API like as ASR3 
API 
> Com_IpduGroupStart 
> Com_IpduGroupStop 
> Com_EnableReceptionDM 
> Com_DisableReceptionDM 
Heiko Hübler 2014-04-25 3.01.00 > Added Chapter: Autosar 3 based I-Pdu 
Group handling 
Markus Bart 2014-06-18 3.01.00 > AR4-601: Support RfC #59936 
(Request Handling) 
Heiko Hübler 2014-06-27 3.01.00 > Added chapter 3.1.2 Signal Processing 
Heiko Hübler 2014-06-27 3.01.01 > ESCAN00076544: The type of the 
parameter "Result" of the APIs 
Com_TpRxIndication and 
Com_TpTxConfirmation mismatches 
between TechRef and source 
Heiko Hübler 2014-11-05 3.02.00 > ESCAN00079371: AR4-698: Post-Build 
Selectable (Identity Manager) 
Heiko Hübler 2015-05-11 3.03.00 > ESCAN00082938: FEAT-1047: 
Gateway Rx signal timeout handling 
without update bits [AR4-894] 
Heiko Hübler 2015-05-20 3.03.01 > ESCAN00083061: The figure on page 
11 is labelled twice. 
Anant Gupta 2015-07-15 4.01.00 > ESCAN00084005: FEAT-77: COM 
Based Transformer for 
CONC_601_SenderReceiverSerializatio
n incl. E2EXf [AR4-829] 
Anant Gupta 2015-12-07 5.00.00 > ESCAN00085557: FEAT-1436 
Gateway: Optimization for COM. 
> ESCAN00087097: FEAT-1442 
Gateway: Routing timeout behaviour 
Gunnar Meiss 2016-02-25 5.01.00 > ESCAN00088555: FEAT-1631: Trigger 
Transmit API with SduLength In/Out 
according to ASR4.2.2 
Gunnar Meiss 
Anant Gupta 
2016-06-05 5.02.00 > ESCAN00090302: FEAT-1688: 
SafeBSW Step 4 
Büsra Bayrak 2016-07-13 5.03.00 > ESCAN00090995: FEAT-1818: 
ComEnableMDTForCyclicTransm

### Page 4

Technical Reference MICROSAR COM 
© 2017 Vector Informatik GmbH Version 6.03.00 4 
based on template version 5.6.0 
> Notification caching and ISR Lock 
Thresholds 
Anant Gupta 2016-07-26 5.03.00 > ESCAN00091171: Missing description 
of Com_Cot.h 
Anant Gupta 2016-08-10 5.03.01 > ESCAN00091398: Update API 
description. 
Büsra Bayrak 2016-09-28 5.04.00 > ESCAN00092101: FEAT-2002: Support 
64 Bit Signal Types for COM according 
to ASR 4.2.2 
Anant Gupta 2016-10-26 5.04.00 > ESCAN00092539: FEAT-1890: 
Extension of gateway description 
routing with shifted copy and update bit 
support. 
Heiko Hübler 2016-11-07 5.04.00 > ESCAN00092684: Tx Timeout for Cyclic 
Messages misses in "Not Supported 
AUTOSAR Standard Conform Features" 
chapter 
Büsra Bayrak 2016-12-09 5.05.00 > FEATC-793: FEAT-2231 Support 
ComTxRepetitionCnt according to ASR 
4.2.2 
Anant Gupta 2017-01-17 5.05.00 > FEATC-797: FEAT-2333: Support Tx 
Timeout for cyclic messages 
Anant Gupta 2017-04-10 6.00.00 > STORYC-18: Support IPDUs without 
IPDU Group assignment in COM 
Büsra Bayrak 2017-04-14 6.00.00 > STORYC-164: Implement 
MASKED_NEW_EQUALS_X and 
MASKED_NEW_DIFFERS_X for Signal 
Group Arrays in Com 
Büsra Bayrak 2017-05-11 6.01.00 > STORYC-694: Implement 
MASKED_NEW_EQUALS_X and 
MASKED_NEW_DIFFERS_X for Signal 
Group Arrays in Com 
Büsra Bayrak 2017-05-17 6.02.00 > STORYC-1205: Rework of COM 
Anant Gupta 2017-07-05 6.03.00 > STORYC-1029: Routing for Group 
Signals with Array Access 
Reference Documents 
No. Source Title Version 
[1] AUTOSAR AUTOSAR_SWS_COM.pdf 4.2.0 
[2] AUTOSAR AUTOSAR_SWS_DevelopmentErrorTracer.pdf 3.2.0 
[3] AUTOSAR AUTOSAR_TR_BSWModuleList.pdf 1.6.0 
[4] Vector TechnicalReference_Asr_Rte.pdf 3.90.00 
[5] Vector TechnicalReference_PostBuildLoadable.pdf 1.0.0

### Page 5

Technical Reference MICROSAR COM 
© 2017 Vector Informatik GmbH Version 6.03.00 5 
based on template version 5.6.0 
 
 
 
Caution 
We have configured the programs in accordance with your specifications in the 
questionnaire. Whereas the programs do support other configurations than the one 
specified in your questionnaire, Vector´s release of the programs delivered to your 
company is expressly restricted to the configuration you have specified in the 
questionnaire.

### Page 6

Technical Reference MICROSAR COM 
© 2017 Vector Informatik GmbH Version 6.03.00 6 
based on template version 5.6.0 
Contents 
1 Component History ................................ ................................ ................................ .... 12 
2 Introduction................................ ................................ ................................ ................. 13 
2.1 Architecture Overview ................................ ................................ ...................... 14 
3 Functional Description ................................ ................................ ............................... 16 
3.1 Features ................................ ................................ ................................ .......... 16 
3.1.1 Signal Types ................................ ................................ .................... 17 
3.1.2 Signal Processing ................................ ................................ ............ 18 
3.1.3 Transmission of a Signal ................................ ................................ .. 18 
3.1.4 Transmission of a Signal Group ................................ ....................... 20 
3.1.5 Transmission Mode Selector ................................ ............................ 22 
3.1.6 Explicit Transmission Mode State Switch ................................ ......... 22 
3.1.7 Transmit Signal Filters ................................ ................................ ...... 23 
3.1.8 Minimum Send Distance of an I-PDU ................................ ............... 24 
3.1.9 Minimum Send Distance only for Direct Send Triggers ..................... 24 
3.1.10 Transmission Deadline Monitoring ................................ ................... 25 
3.1.11 Replication of Signal Transmission Requ

### Page 7

Technical Reference MICROSAR COM 
© 2017 Vector Informatik GmbH Version 6.03.00 7 
based on template version 5.6.0 
3.1.24.4 Main Function Timing Domains ................................ ...... 39 
3.1.24.4.1 Timebase for Rx-deadline monitoring 
handling ................................ ..................... 40 
3.1.24.4.2 Timebase for Tx-deadline monitoring 
handling ..........

*Excerpt: first 8 of 85 pages shown.*
