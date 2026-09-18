---
title: '_Bmw_5441_Eps_Impl_A — AN-ISC-8-1184_Compiler_Warnings'
description: 'Converted PDF document AN-ISC-8-1184_Compiler_Warnings.pdf from module _Bmw_5441_Eps_Impl_A.'
sidebar:
  hidden: true
---

> **Source:** `AN-ISC-8-1184_Compiler_Warnings.pdf` (PDF, 395 KB, in-module path `doc/`)
>
> Converted from PDF with text extraction; layout, vector diagrams and scanned figures are not preserved. See the source PDF in the repository for the authoritative content.
>
> pages: 8; title: Compiler Warnings; author: Andreas Raisch

## Converted content

### Page 1

Compiler Warnings 
Version 1.0 
2015 -11-02 
Application Note AN-ISC -8-1184 
Author Andreas Raisch 
Restrictions Customer confidential – Vector decides 
Abstract Warning free code is an important quality goal for embedded software. Nevertheless, 
compiler warnings can occur for highly configurable software. Typical compiler 
warnings are listed and justified within this document. 
 
 
Table of Contents 
1 Overview ........................................................................................................................................ 2 
1.1 Deviation Procedure ............................................................................................................ 3 
1.2 Default BSW Delivery Process ............................................................................................ 3 
2 Accepted Deviations ..................................................................................................................... 3 
2.1 Unused/unreferenced parameter/argument ......................................................................... 4 
2.2 Unused/unreferenced define, enum value ........................................................................... 4 
2.3 Unused/unreferenced variable ............................................................................................. 4 
2.4 Unused/unreferenced function ............................................................................................. 5 
2.5 Condition evaluates always to true/false ............................................................................. 5 
2.6 Unreachable code/statement ............................................................................................... 6 
2.7 Dead assignment / variable set but not used ...........................

### Page 2

Compiler Warnings 
 
Copyright © 2015 - Vector Informatik GmbH 2 
Contact Information: www.vector.com or +49-711-80 670-0 
1 Overview 
MICROSAR BasicSoftware (BSW) is developed in a product line approach, independent from specific 
ECU projects or compilers. MICROSAR BSW supports the AUTOSAR MemoryAbstraction and 
CompilerAbstraction concepts and supports a huge range of different compiler vendors, versions and 
options. 
MICROSAR BSW is delivered as static source code and code generators to support the ECU project 
specific adaption and optimization of the BSW behavior and feature set based on AUTOSAR 
configuration files and user defined selections. 
Additionally, MICROSAR BSW supports compile time configuration, link time configuration and post-
build configuration. 
 
Figure 1 MICROSAR BSW Component 
A general quality goal for MICROSAR BSW is “warning free code”. The coding style guide for 
MICROSAR BSW is based on MISRA-C:2004. Checks for MISRA compliance are an essential part of 
our development process. Based on “HIS Gemeinsames Subset der MISRA C Guidelines v2.0“ 
(http://www.automotive-his.de) all rules are active. 
Nevertheless, we accept deviations to the “warning free code” goal based on the here defined list of 
exceptions. Known and accepted deviations are reported within the delivery as ESCAN type “Warning 
in released product”. 
Document [2] explains the relationship between user-selected code generation (optimization) options 
and compiler warnings.

### Page 3

Compiler Warnings 
 
Copyright © 2015 - Vector Informatik GmbH 3 
Contact Information: www.vector.com or +49-711-80 670-0 
1.1 Deviation Procedure 
Priority Rule Rationale 
1 
MICROSAR BSW shall be compiler 
warning free. Thus, compiler warnings 
shall be prevented wherever possible. 
Detection of compiler warning either during 
component development or more frequently 
when applying the customer specific 
compiler/options/BSW configuration during 
the delivery tests. 
2 
If a compiler warning is detected, the code 
shall be analyzed and, if reasonable, be 
changed/extended to become warning 
free. 
We want to prevent to deliver defect code to 
our customers. We also need to take into 
account e.g. runtime efficiency, maintainability 
and standardized code for many use-cases. 
3 
If fixing the compiler warning is not a 
solution, an ESCAN of type “Warning in 
released product” shall be created to 
document the accepted deviation also in 
the report of known issues of deliveries. 
See list of accepted deviations in this 
document. 
Table 1 Priority of measures to prevent compiler warnings 
 
1.2 Default BSW Delivery Process 
The configuration and compilation and linkage during the delivery test activities yield most of the 
compiler warnings, because the development tool chain and settings specified by you are used. 
The process in short is: 
> Customer specifies the compiler brand, version and options (via Questionnaire) and provides 
more information on the expected use-case 
> Delivery engineer creates example configurations of the BSW and compiles and links the outcome 
> Compiler warnings are analyzed and either documented as ESCAN of type “Warning in released 
product” or reported to the development teams to trigger a fix. 
> ESCANs of type “Issue in released produ

### Page 4

Compiler Warnings 
 
Copyright © 2015 - Vector Informatik GmbH 4 
Contact Information: www.vector.com or +49-711-80 670-0 
2.1 Unused/unreferenced parameter/argument 
Deviation ID CW_001 
Example compiler 
warning strings 
„Unreferenced formal parameters“, „parameter is never used“, „has no-used 
argument“ 
Reason BSW provides APIs as described by standards. Not all parameters are 
necessary and used within the function in all possible usage scenarios. 
Configuration 
dependent 
Yes 
Potential risk The function contains unused code. 
Prevention of risk Code inspection has to check that the unused code is not critical concerning 
the expected behavior. Small increase of ROM footprint is accepted. 
Note 
Workarounds for suppressing such compiler warnings often conflict with 
MISRA-C:2004, rule 14.2 (See MISRA Compliance Documentation, Deviation 
ID MD_MSR_14.2) 
Table 2 CW_001 
2.2 Unused/unreferenced define, enum value 
Deviation ID CW_002 
Example compiler 
warning strings 
„Unused enumeration values“, „Unused define value“ 
Reason Encapsulation of defines, enum-values and similar items for multiple complex 
configuration data sets (via #ifdef) reduces readability and maintainability. 
Configuration 
dependent 
Yes 
Potential risk Defined but never used enums or defines may decrease readability and 
maintainability. 
Prevention of risk Execution of runtime tests with different configuration variants. 
Note - 
Table 3 CW_002 
2.3 Unused/unreferenced variable 
Deviation ID CW_003 
Example compiler 
warning strings 
„unreferenced local variable within abc.c“, „variable "abc" was declared but 
never referenced“, „Variables related to message supervision are set but 
never used“ 
Reason 
Because of goal "minimize RAM footprint", unused variables shall be disabled 
via #ifdef

### Page 5

Compiler Warnings 
 
Copyright © 2015 - Vector Informatik GmbH 5 
Contact Information: www.vector.com or +49-711-80 670-0 
2.4 Unused/unreferenced function 
Deviation ID CW_004 
Example compiler 
warning strings 
„Declared but unused function abc“, „unused static function abc“ 
Reason 
BSW provides APIs as described by standard. 
Because of goal "minimize ROM footprint", unused functions shall be 
disabled via #ifdef based on configuration data sets. 
Not all provided functions might be used in the concrete ECU project 
(configuration and usage dependent). Encapsulation for multiple complex 
configuration data sets (via #ifdef) reduces readability and maintainability and 
is thus not provided on a per-function base for all APIs. 
Configuration 
dependent 
Yes 
Potential risk The project contains unused code. 
Prevention of risk See “Reason” 
Note Partly addressed by MISRA-C:2004, rule 8.10 (See MISRA Compliance 
Documentation, Deviation ID MD_MSR_8.10) 
Table 5 CW_004 
2.5 Condition evaluates always to true/false 
Deviation ID
