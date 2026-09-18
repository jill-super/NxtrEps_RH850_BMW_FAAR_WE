---
title: '_Bmw_5441_Eps_Impl_A — DVCfg_AutomationInterfaceDocumentation'
description: 'Converted PDF document DVCfg_AutomationInterfaceDocumentation.pdf from module _Bmw_5441_Eps_Impl_A.'
sidebar:
  hidden: true
---

> **Source:** `DVCfg_AutomationInterfaceDocumentation.pdf` (PDF, 3199 KB, in-module path `doc/`)
>
> Converted from PDF with text extraction; layout, vector diagrams and scanned figures are not preserved. See the source PDF in the repository for the authoritative content.
>
> pages: 284; title: DaVinci Configurator AutomationInterface Documentation; author: DaVinci Configurator Team

## Converted content

### Page 1

DaVinci Conﬁgurator AutomationInterface
Development Documentation of the AutomationInterface (AI)
DaVinci Conﬁgurator Team
January 18, 2018
© 2018
Vector Informatik GmbH
Ingersheimerstr. 24
70499 Stuttgart

### Page 2

Contents
1 Introduction 10
1.1 General . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 10
1.2 Facts . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 10
2 Getting started with Script Development 11
2.1 General . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 11
2.2 Automation Script Development Types . . . . . . . . . . . . . . . . . . . . . . . . 11
2.3 Script File . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 11
2.4 Script Project . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 13
2.4.1 Script Project Development . . . . . . . . . . . . . . . . . . . . . . . . . . 15
2.4.2 Java JDK Setup . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 16
2.4.3 IntelliJ IDEA Setup . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 16
2.4.4 Gradle Setup . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 17
3 AutomationInterface Architecture 18
3.1 Components . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 18
3.2 Languages . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 19
3.2.1 Why Groovy . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 19
3.3 Script Structure . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 20
3.3.1 Scripts . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 20
3.3.2 Script Tasks . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 21
3.3.3 Script Locations . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 21
3.4 Script loading . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 21
3.

### Page 3

Contents
4.4.1 Execution Context . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 34
4.4.1.1 Code Block Arguments . . . . . . . . . . . . . . . . . . . . . . . 35
4.4.2 Task Execution Sequence . . . . . . . . . . . . . . . . . . . . . . . . . . . 35
4.4.3 Script Path API during Execution . . . . . . . . . . . . . . . . . . . . . . 36
4.4.3.1 Path Resolution by Parent Folder . . . . . . . . . . . . . . . . . 37
4.4.3.2 Path Resolution . . . . . . . . . . . . . . . . . . . . . . . . . . . 37
4.4.3.3 Script Folder Path Resolution . . . . . . . . . . . . . . . . . . . 38
4.4.3.4 Project Folder Path Resolution . . . . . . . . . . . . . . . . . . . 38
4.4.3.5 SIP Folder Path Resolution . . . . . . . . . . . . . . . . . . . . . 39
4.4.3.6 Temp Folder Path Resolution . . . . . . . . . . . . . . . . . . . . 39
4.4.3.7 Other Project and Application Paths . . . . . . . . . . . . . . . 40
4.4.4 Script logging API . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 40
4.4.5 User Interactions and Inputs . . . . . . . . . . . . . . . . . . . . . . . . . 41
4.4.5.1 UserInteraction . . . . . . . . . . . . . . . . . . . . . . . . . . . . 41
4.4.5.2 Progress Indication . . . . . . . . . . . . . . . . . . . . . . . . . 42
4.4.6 Script Error Handling . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 44
4.4.6.1 Script Exceptions . . . . . . . . . . . . . . . . . . . . . . . . . . 44
4.4.6.2 Script Task Abortion by Exception . . . . . . . . . . . . . . . . . 44
4.4.6.3 Unhandled Exceptions from Tasks . . . . . . . . . . . . . . . . . 45
4.4.7 User deﬁned Classes and Methods . . . . . . . . . . . . . . . . . . . . . . 46
4.4.8 Usage of Automation API in own deﬁned Classes and Methods . . . . . . 47
4.4.8.1 Access the Automation API like the Script code{} Block . 

### Page 4

Contents
4.6.2.4 Write the SystemDescription . . . . . . . . . . . . . . . . . . . . 77
4.6.3 BswmdModel in AutomationInterface . . . . . . . . . . . . . . . . . . . . 79
4.6.3.1 BswmdModel Package and Class Names . . . . . . . . . . . . . . 79
4.6.3.2 Reading with BswmdModel . . . . . . . . . . . . . . . . . . . . . 79
4.6.3.3 Writing with BswmdModel . . . . . . . . . . . . . . . . . . . . . 80
4.6.3.4 Sip DefRefs . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 81
4.6.3.5 BswmdModel DefRefs . . . . . . . . . . . . . . . . . . . . . . . . 81
4.6.3.6 Switching from Domain Models to BswmdModel . . . . . . . . . 82
4.6.4 MDF Model in AutomationInterface . . . . . . . . . . . . . . . . . . . . . 82
4.6.4.1 Reading the MDF Model . . . . . . . . . . . . . . . . . . . . . . 83
4.6.4.2 Reading the MDF Model by String . . . . . . . . . . . . . . . . . 85
4.6.4.3 Writing the MDF Model . . . . . . . . . . . . . . . . . . . . . . 87
4.6.4.4 Simple Property Changes . . . . . . . . . . . . . . . . . . . . . . 87
4.6.4.5 Creating single Child Members (0:1) . . . . . . . . . . . . . . . . 88
4.6.4.6 Creating and adding Child List Members (0:*) . . . . . . . . . . 88
4.6.4.7 Updating existing Elements . . . . . . . . . . . . . . . . . . . . . 91
4.6.4.8 Deleting Model Objects . . . . . . . . . . . . . . . . . . . . . . . 92
4.6.4.9 Duplicating Model Objects . . . . . . . . . . . . . . . . . . . . . 92
4.6.4.10 Special properties and extensions . . . . . . . . . . . . . . . . . . 93
4.6.4.11 Reverse Reference Resolution - ReferencesPointingToMe . . . . . 95
4.6.4.12 Derived Containers . . . . . . . . . . . . . . . . . . . . . . . . . 95
4.6.4.13 AUTOSAR Root Object . . . . . . . . . . . . . . . . . . . . . . 96
4.6.4.14 ActiveEcuC . . . . . . . . . . . . . . . . . . . . . . .

### Page 5

Contents
4.8.3 Model Transaction and Validation-Result Invalidation . . . . . . . . . . . 121
4.8.4 Solve Validation-Results with Solving-Actions . . . . . . . . . . . . . . . . 121
4.8.4.1 Solver API . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 122
4.8.5 Advanced Topics . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 124
4.8.5.1 Access Validation-Results of a Model Object . . . . . . . . . . . 124
4.8.5.2 Access Validation-Results of a DefRef . . . . . . . . . . . . . . . 124
4.8.5.3 Filter Validation-Results using an ID Constant . . . . . . . . . . 125
4.8.5.4 Identiﬁcation of a Particular Solving-Action . . . . . . . . . . . . 125
4.8.5.5 Validation-Result Description as MixedText . . . . . . . . . . . . 126
4.8.5.6 Further IValidationResultUI Methods . . . . . . . . . . . . . . . 126
4.8.5.7 IValidationResultUI in a variant (Post Build Selectable) Project 127
4.8.5.8 Erroneous CEs of a Validation-Result . . . . . . . . . . . . . . . 127
4.8.5.9 Examine Solving-Action Execution . . . . . . . . . . . . . . . . . 129
4.8.5.10 Create a Validation-Result in a Script Task . . . . . . . . . . . . 130
4.8.5.11 Turn oﬀ auto-solving-action execution . . . . . . . . . . . . . . . 132
4.9 Update Workﬂow . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 133
4.9.1 Method Overview . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 133
4.9.2 Example: Content of Input Files has changed. . . . . . . . . . . . . . . . . 133
4.9.3 Example: List of Input Files shall be changed . . . . . . . . . . . . . . . . 134
4.9.4 Prerequisites . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 134
4.10 Domains . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 136
4.10.1 Communication D

### Page 6

Contents
4.13.2.2 Execution of Spock Tests . . . . . . . . . . . . . . . . . . . . . . 199
4.13.2.3 Registration of Unit Tests in Scripts . . . . . . . . . . . . . . . . 199
5 Data models in detail 201
5.1 MDF model - the raw AUTOSAR data . . . . . . . . . . . . . . . . . . . . . . . 201
5.1.1 Naming . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 201
5.1.2 The models inheritance hiearchy . . . . . . . . . . . . . . . . . . . . . . . 201
5.1.2.1 MIObject and MDFObject . . . . . . . 

*Excerpt: first 8 of 284 pages shown.*
