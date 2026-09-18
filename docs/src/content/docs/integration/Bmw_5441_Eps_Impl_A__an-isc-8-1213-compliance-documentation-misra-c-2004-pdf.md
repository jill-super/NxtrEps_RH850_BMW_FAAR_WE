---
title: '_Bmw_5441_Eps_Impl_A — AN-ISC-8-1213_Compliance Documentation MISRA-C_2004'
description: 'Converted PDF document AN-ISC-8-1213_Compliance Documentation MISRA-C_2004.pdf from module _Bmw_5441_Eps_Impl_A.'
sidebar:
  hidden: true
---

> **Source:** `AN-ISC-8-1213_Compliance Documentation MISRA-C_2004.pdf` (PDF, 717 KB, in-module path `doc/`)
>
> Converted from PDF with text extraction; layout, vector diagrams and scanned figures are not preserved. See the source PDF in the repository for the authoritative content.
>
> pages: 26; title: Compliance Documentation MISRA-C:2004; author: Andreas Raisch

## Converted content

### Page 1

Compliance Documentation MISRA -C:2004 
Version 3.0 
2017 -10-09 
Application Note AN-ISC -8-1213 
Author Andreas Raisch 
Restrictions Customer Confidential – Vector decides 
Abstract This document explains the MISRA-C and HIS Metric compliance enforcement. It also 
contains the project specific MISRA and code metric deviations including their 
justifications. 
 
 
Table of Contents 
1 Overview ........................................................................................................................................ 3 
1.1 Purpose, goal ....................................................................................................................... 3 
2 Enforcing MISRA-C Compliance .................................................................................................. 4 
2.1 Software Engineering Context ............................................................................................. 4 
2.2 Programming Language and Coding Context ..................................................................... 4 
2.3 Project specific MISRA Subset ............................................................................................ 4 
2.4 MISRA Compliance Matrix ................................................................................................... 4 
2.5 Hints on Compiler Selection ................................................................................................. 6 
2.5.1 Deactivated QA-C Rules for MICROSAR Product Analysis ................................................ 7 
2.6 Deviation Procedure ............................................................................................................ 7 
2.7 Usage of C99 Features ..........................................................................

### Page 2

Compliance Documentation MISRA-C:2004 
Copyright © 2017 - Vector Informatik GmbH 2 
Contact Information: www.vector.com or +49-711-80 670-0 
Revision List 
Version Editor Date Section Changes, Comments 
0.1.0 virTsd 2009-03-31 all Initial version 
1.0.0 visRa 2011-04-26 Reference
s 
References changed to new locations on server 
1.1.0 visRa 2012-02-17 Deviations New project deviations added: MD_MSR_1.1_810, 
MD_MSR_1.1_828, MD_MSR_1.1_857 
2.0.0 visRa 2013-04-22 all Document renamed due to new target “claiming 
compliance”. Completely reworked; new chapters 
“Enforcing MISRA-C Compliance” and “Enforcing 
Code Metric” added. MISRA product deviations 
moved in appendix; code metric deviations added. 
2.1.0 visRa 2013-12-16 Chapter “Hints on Compiler Selection” added; new 
standard deviations added in “MISRA Justification 
for “Project Deviations”: MD_MSR_1.1_639, 
MD_MSR_5.1_777, MD_MSR_19.13_0342 
2.2.0 visRa 2014-03-19 Chapter “Hints on Compiler Selection” extended; 
new standard deviations added in “MISRA 
Justification for “Project Deviations”: 
MD_MSR_1.1_715 and MD_MSR_5.1_779 
2.3.0 visRa 2015-02-18 New standard deviation MD_MSR_14.2 added 
New standard deviation MD_MSR_5.7 added 
QA-C rule 850 deactivation added to chapter 2.4 
MISRA Compliance Matrix 
2.4.0 visRa 2016-04-08 Chapter 2.7 Usage of C99 Features added 
2.5.0 visRa 2016-10-13 New standard deviation MD_MSR_16.7 added 
Mapping to [MISRA-P1] added 
2.6.0 visRa 2017-02-03 New standard deviation MD_MSR_5.6 added 
3.0.0 visRa 2017-10-06 Migration to “application note” format 
Usage and justification rule 14.7 adapted to Vector 
SafeBSW “process 3”.

### Page 3

Compliance Documentation MISRA-C:2004 
Copyright © 2017 - Vector Informatik GmbH 3 
Contact Information: www.vector.com or +49-711-80 670-0 
1 Overview 
1.1 Purpose, goal 
The purpose of this document is to explain the process executed and limitations known to claim 
compliance of the product MICROSAR to “MISRA-C:2004 guidelines for the use of the C language in 
critical systems” [MISRA-C] and to HIS source code metrics [HIS-CODE]. 
In addition, the document also describes the handling of code metrics. 
The products are developed in a product-line approach, so the wording “project” in [MISRA-C] is 
mapped to “product” in this context, too. Product-line approach means that a large set of reusable 
software-components are developed and maintained to fulfill the functional needs of different O EMs 
and TIER1s for any ECU in any vehicle. 
 
 
Figure 1-1 Overall MISRA process: MISRA standard – code style guides – code – compliance matrix - … 
 
Own 
rules
List of 
project-
specific 
deviations
Req
Adv
CodeStyle Guide
Compliance Matrix
Code Verification
by tool
Verification
by review
rules
Req
Code 
Template
(+QA-C markers)
(+Specific 
deviation 
justification)

### Page 4

Compliance Documentation MISRA-C:2004 
Copyright © 2017 - Vector Informatik GmbH 4 
Contact Information: www.vector.com or +49-711-80 670-0 
2 Enforcing MISRA-C Compliance 
2.1 Software Engineering Context 
If not otherwise stated, the product is developed according AUTOMOTIVE SPICE, level 3. 
2.2 Programming Language and Coding Context 
Used programing languages are 
> C99 but using C90 subset only (see chapter 2.7 Usage of C99) 
> ASM (rarely used, only for µC-specific codes like ISR, register access, ...) 
Code is developed based on a code style guide and by applying code and header templates. 
Selected code metrics are measured, documented and deviations are justified. 
Runtime test coverage is measured, documented and deviations are justified. 
2.3 Project specific MISRA Subset 
[HIS-MISRA] defines all rules to be “required”, so no rule is “advisory”. 
All 141 rules in [MISRA-C] are analyzed for product relevance. If a rule is judged to be not relevant, it 
is justified in chapter 2.4 MISRA Compliance Matrix. 
2.4 MISRA Compliance Matrix 
The compliance matrix for the product is: 
> All rules not explicitly listed in Table 2-1 are checked by the tool QA-C (125 rules) 
> Rules listed in Table 2-1 and marked “Code inspection” are manually checked (8 rules) 
> Rules listed in Table 2-1 and marked “Not applicable” are not checked (8 rules); the justification is 
added within the table. 
Rule Description Enforcement Strategy 
1.3 
(req) 
 
Multiple compilers and/or languages shall only be 
used if there is a common defined interface standard 
for object code to which the 
languages/compilers/assemblers conform. 
Not applicable 
Justification: Multiple compilers or 
languages are not used in embedded 
software components developed at 
PES. The only exception is the usage

### Page 5

Compliance Documentation MISRA-C:2004 
Copyright © 2017 - Vector Informatik GmbH 5 
Contact Information: www.vector.com or +49-711-80 670-0 
Rule Description Enforcement Strategy 
 
Note 
[MISRA-P1] addresses 
this topic in 
Permit/MISRA/C:2004/5.1
.A.1. 
 
 
1.5 
(adv) 
 
Floating-point implementations should comply with a 
defined floating-point standard. 
Not applicable 
Justification: Floating point operations 
are not used in embedded software 
components developed at PES. 
2.4 
(adv) 
 
Sections of code should not be ‘commented out’. Code inspection 
3.2 
(req) 
 
The character set and the corresponding encoding 
shall be documented. 
Not applicable 
Justification: Character strings are not 
used in embedded software 
components developed at PES. 
3.3 
(adv) 
 
The implementation of integer division in the chosen 
compiler should be determined, documented and 
taken into account. 
Comment: There is a potential issue in case of the 
division of negative signed integers because the 
compiler behavior is not standardized. 
Not applicable 
Justification: Division of negative 
signed integers is not used in 
embedded software components 
developed at PES. 
3.5 
(req) 
 
If it is being relied upon, the implementation-defined 
behavior and packing of bit-fields shall be 
documented. 
Not applicable 
Justification: In the embedded 
environment the handling of bit-fields 
is documented for each compiler and 
hardware in the compilers’ user 
manual. Beyond this, tests minimize 
the risk indicated by t

*Excerpt: first 8 of 26 pages shown.*
