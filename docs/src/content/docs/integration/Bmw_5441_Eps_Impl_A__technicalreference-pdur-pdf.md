---
title: '_Bmw_5441_Eps_Impl_A — TechnicalReference_PduR'
description: 'Converted PDF document TechnicalReference_PduR.pdf from module _Bmw_5441_Eps_Impl_A.'
sidebar:
  hidden: true
---

> **Source:** `TechnicalReference_PduR.pdf` (PDF, 1689 KB, in-module path `doc/`)
>
> Converted from PDF with text extraction; layout, vector diagrams and scanned figures are not preserved. See the source PDF in the repository for the authoritative content.
>
> pages: 71; title: MICROSAR PDU Router; author: Erich Schondelmaier, Gunnar Meiss, Sebastian Waldvogel, Florian Röhm

## Converted content

### Page 1

MICROSAR PDU Router 
Technical Reference 
 
DaVinci Configurator 
Version 3.00.01 
 
 
 
 
 
 
 
 
 
 
 
Authors Erich Schondelmaier, Gunnar Meiss, Sebastian 
Waldvogel, Florian Röhm 
Status Released

### Page 2

Technical Reference MICROSAR PDU Router 
© 2017 Vector Informatik GmbH Version 3.00.01 2 
based on template version 4.9.2 
Document Information 
History 
Author Date Version Remarks 
Erich Schondelmaier 2012-12-20 1.00.00 Initial version based on PduR Technical 
Reference 
Erich Schondelmaier 2012-07-12 2.00.00 Adapted to AUTOSAR 4.0.3 
Erich Schondelmaier 2012-10-15 2.01.00 TP Gateway 
IF Gateway 
Gunnar Meiss 2012-11-21 2.02.00 AR4-285: Support PduRRoutingPathGroups 
Erich Schondelmaier 2013-02-07 2.02.01 Adapted Tp- API description 
Erich Schondelmaier 2013-02-15 2.02.02 Added some ASR deviations 
ESCAN00064126 
Erich Schondelmaier 2013-03-19 2.03.00 ESCAN00064364 AR4-325: Post-Build 
Loadable 
Added Cancel- Receive/ Transmit Support 
Erich Schondelmaier 2014-04-15 2.04.00 Added TP routing with variable addresses 
(MetaData Handling) 
Added Threshold “0” support 
Erich Schondelmaier 2014-04-15 2.04.01 Support the StartOfReception API (with the 
PduInfoType), 
TxConfirmation and RxIndication according 
ASR4.1.2 
Erich Schondelmaier 2014-09-01 2.05.00 Added SecOC to the Interface Overview 
Extended Tp Gateway Routing behavior 
description 
Updated Configuration Variant 
Sebastian Waldvogel 2015-02-23 2.06.00 FEAT-1057: Added documentation about 
configuration of range rou ting paths and 
functional requests gateway 
Sebastian Waldvogel 2015-05-11 2.06.01 FEAT-1057: Improvements of documentation 
Florian Röhm 2015-07-30 2.07.00 FEAT-109: Added documentation for PduR 
switching feature and N:1 routing paths 
Florian Röhm 2016-01-16 2.08.00 FEAT-1485: Added documentation for 1:N 
and N:1 transport protocol routing paths 
Gunnar Meiss 2016-02-25 2.08.00 FEAT-1631: Trigger Transmit API with 
SduLength In/Out according to ASR4.2.2 
Erich Schondelmaier 2016-03-17 2.08.00 adde

### Page 3

Technical Reference MICROSAR PDU Router 
© 2017 Vector Informatik GmbH Version 3.00.01 3 
based on template version 4.9.2 
Florian Röhm 2016-04-01 2.08.01 Removed empty chapters 
Erich Schondelmaier, 
Florian Röhm 
2016-08-10 3.00.00 Shared/Dedicated Buffer support 
Memory mapping extension 
Sebastian Waldvogel 2016-11-24 3.00.00 Smart Learning (Switching) 
Florian Röhm 2017-06-22 3.00.01 ESCAN00095254: Missing DET error 
PDUR_E_PDU_INSTANCES_LOST 
description in case of N:1 communication 
interface routings with upper layer 
Florian Röhm 2017-06-23 3.00.01 STORYC-1629: N:1 routing path support for 
IpduM Container feature

### Page 4

Technical Reference MICROSAR PDU Router 
© 2017 Vector Informatik GmbH Version 3.00.01 4 
based on template version 4.9.2 
Reference Documents 
No. Source Title Version 
[1] AUTOSAR AUTOSAR_SWS_PDURouter.pdf 4.0.3 
[2] AUTOSAR AUTOSAR_SWS_PDURouter.pdf. 4.1.1 
[3] AUTOSAR AUTOSAR_SWS_PDURouter.pdf 4.1.2 
[4] AUTOSAR AUTOSAR_SWS_DevelopmentErrorTracer.pdf 3.2.0 
[5] AUTOSAR AUTOSAR_TR_BSWModuleList.pdf 1.6.0 
[6] AUTOSAR AUTOSAR_SWS_SAEJ1939TransportLayer.pdf 1.5.0 
[7] Vector TechnicalReference_CanIf.pdf 6.02.00 
[8] Vector TechnicalReference_<CAN Driver>.pdf - 
[9] AUTOSAR TechnicalReference_CanTp.pdf 2.00.00 
 
This technical reference describes the general use of the PduR basis software module. 
 
 
 
 
Caution 
We have configured the programs in accordance with your specifications in the 
questionnaire. Whereas the programs do support other configurations than the one 
specified in your questionnaire, Vector´s release of the programs delivered to your 
company is expressly restricted to the configuration you have specified in the 
questionnaire.

### Page 5

Technical Reference MICROSAR PDU Router 
© 2017 Vector Informatik GmbH Version 3.00.01 5 
based on template version 4.9.2 
Contents 
1 Component History ................................ ................................ ................................ .... 10 
2 Introduction................................ ................................ ................................ ................. 11 
2.1 Architecture Overview ................................ ................................ ...................... 12 
3 Functional Description ................................ ................................ ............................... 14 
3.1 Features ................................ ................................ ................................ .......... 14 
3.2 Interfaces to adjacent modules of the PDUR ................................ .................... 15 
3.3 Initialization ................................ ................................ ................................ ...... 15 
3.4 States ................................ ................................ ................................ .............. 15 
3.5 Error Handling ................................ ................................ ................................ .. 15 
3.5.1 Development Error Reporting ................................ ........................... 15 
3.6 Interface Layer Gateway ................................ ................................ .................. 15 
3.6.1 Data Provision ................................ ................................ .................. 15 
3.6.1.1 Direct data provision ................................ ...................... 15 
3.6.1.2 Trigger transmit data provision ................................ ....... 16 
3.6.2 FIFO Queue .........................

### Page 6

Technical Reference MICROSAR PDU Router 
© 2017 Vector Informatik GmbH Version 3.00.01 6 
based on template version 4.9.2 
3.7.3.1.1 Dedicated Tx Buffer ................................ ... 29 
3.7.3.1.2 Shared Tx Buffer ................................ ........ 29 
3.7.3.1.3 Local Tx Buffer Pool ................................ ... 30 
3.7.3.1.4 Global Tx Buffer Pool ................................ . 30 
3.7.3.2 Example Configuration ................................ ................... 30 
3.7.3.3 Tx Buffer Length Configuration ................................ ...... 31 
3.7.3.4 Amount of Tx Buffer ................................ ....................... 31 
3.7.3.5 Tx Buffer Selection Algorithm ................................ ......... 32 
3.7.4 TP Queue ................................ ................................ ........................ 32 
3.7.5 Error Handling ................................ ................................ .................. 32 
3.7.6 Meta Data Handling ................................ ................................ ......... 33 
4 Integration ................................ ................................ ................................ ................... 34 
4.1 Scope of Delivery ................................ ................................ ............................. 34 
4.1.1 Static Files ................................ ................................ ....................... 34 
4.1.2 Dynamic Files ................................ ................................ .................. 34 
4.2 Critical Sections ................................ ................................ ............................... 35 
4.3 Memory Sections ................................ ................................ ............................. 

### Page 7

Technical Reference MICROSAR PDU Router 
© 2017 Vector Informatik GmbH Version 3.00.01 7 
based on template version 4.9.2 
5.4.7 PduR_<GenericLo>TpTxConfirmation ................................ ............. 46 
5.4.8 PduR_<GenericLo>TpRxIndication ................................ .................. 47 
5.4.9 PduR_<GenericUpTp>Transmit ................................ ....................... 48 
5.5 Service Ports ................................ ................................ ................................ ... 49 
5.5.1 Complex Device Driver Interaction ................................ ............

*Excerpt: first 8 of 71 pages shown.*
