---
title: '_Bmw_5441_Eps_Impl_A — Startup_BMW_BAC40'
description: 'Converted PDF document Startup_BMW_BAC40.pdf from module _Bmw_5441_Eps_Impl_A.'
sidebar:
  hidden: true
---

> **Source:** `Startup_BMW_BAC40.pdf` (PDF, 7997 KB, in-module path `doc/`)
>
> Converted from PDF with text extraction; layout, vector diagrams and scanned figures are not preserved. See the source PDF in the repository for the authoritative content.
>
> pages: 217; title: Startup with BMW BAC4.x; author: Vector Informatik GmbH (Klaus Emmert, Manuela Huber)

## Converted content

### Page 1

StartupwithBMW BAC4.x
Version13.0.1 forMICROSAR 4Release19

### Page 2

©VectorInformatikGmbH Version13.0.1forRelease19 -2-
Content
1AboutThisManual 11
1.1HistoryInformation 11
1.2FindingInformationQuickly 11
1.3Conventions 11
1.4Certification 12
1.5Warranty 12
1.6Support 13
1.7Trademarks 13
1.8ErrataSheetofHardwareManufacturers 14
1.9ExampleCode 14
1.10WhatDoYouLearnfromThisManual 14
2Basics 16
2.1AnOverallView 16
2.2MICROSAR-Vector'sAUTOSAR Solution 17
2.3AUTOSARLayerModelBMW 17
ISTEPbySTEP 19
1STEP1SetupYourProject 20
1.1SituationafterInstallation 20
1.2SetupProjectviaDaVinciConfiguratorPro 20
1.2.1GeneralSettings 21
1.2.2ProjectFolderStructure 21
1.2.3Target 21
1.2.4DaVinciDeveloper 22
1.3ResultProjectFolder-ResultoftheProjectSetup 23
1.3.1Applfolder 23
1.3.2Configfolder 23
1.3.3<ProjectName>.dpa 24
1.3.4LogFolder 24
1.4StartMenu-ResultoftheProjectSetup 25
1.5DaVinciConfiguratorProProject 25
Content UserManualStartupwithBMWBAC4.x

### Page 3

2STEP2DefineProjectSettings 26
2.1AddInputFiles 26
2.1.1AddSystemDescriptionFiles 26
2.1.2AddDiagnosticDataFiles 28
2.1.3StateDescription 30
2.1.4AddStandardConfigurationFiles 32
2.1.5DefineOptionsforInputFiles 32
2.1.6UpdateConfiguration 32
2.2DefineExternalGenerationStepsandSWCTemplatesandContractPhaseHeaders 35
2.2.1ExternalGenerationSteps 35
2.2.2SWC TemplatesandContractPhaseHeaders 36
2.3AddorUpdateBACModules 37
2.4ActivateYourBSWModules 37
2.5AddECUCFileReferences 38
2.6ChangeProjectSettings 38
2.6.1PostbuildSupport 39
3STEP3Validation 40
3.1StartSolveAllMechanism 40
3.2LiveValidation-SolvingActions 40
4STEP4StartBSWConfiguration 42
4.1StartConfigurationwithConfigurationEditors 42
4.2BaseServices 42
4.2.1DefaultErrorTracer 42
4.2.2GeneralPurposeTimer(GPT) 42
4.2.3RAM Test 42
4.3Communication 43
4.3.1CommunicationGeneral 43
4.3.2BusController 43
4.3.3PDUs 43
4.3.4Signals 44
©VectorInformatikGmbH Version13.0.1forRelease19 -3-
Content UserManualStartupwithBMWBAC4.x

### Page 4

©VectorInformatikGmbH Version13.0.1forRelease19 -4-
4.3.5SocketAdapterUsers 44
4.3.6TransportProtocol 44
4.4Diagnostics 44
4.4.1DiagnosticDataIdentifiers 44
4.4.2DiagnosticEventData 44
4.4.3DiagnosticEvents 44
4.4.4ProductionErrorHandling 45
4.4.5AddDiagnosticDataID Assistant 45
4.4.6AutomapDiagnosticDataObjects 46
4.4.7SetupEventMemoryBlocks 46
4.5I/O 46
4.5.1IO HardwareAbstraction 46
4.6Memory 46
4.6.1MemoryGeneral 46
4.6.2MemoryBlocks 46
4.6.3OptimizeFee 47
4.7ModeManagementEditors 47
4.7.1BSWManagement 47
4.7.2ActivateInterruptsofPeripheralsDevices 50
4.7.3ECUManagement 53
4.7.4Initialization 53
4.7.5Watchdogs 53
4.8NetworkManagement 54
4.8.1NetworkManagementGeneral 54
4.8.2CommunicationUsers 54
4.8.3PartialNetworking 54
4.9RuntimeSystem 55
4.9.1RuntimeSystemGeneral 55
4.9.2ECUSoftwareComponents 55
4.9.3ModuleInternalBehavior 56
Content UserManualStartupwithBMWBAC4.x

### Page 5

4.9.4OSConfiguration 56
4.9.5TaskMapping 56
4.10GoonwithBasicEditor 57
4.11StartSolvingActions 57
4.12StartOn-demandValidation 57
4.13BSW Configurationfinished 59
5STEP5DesignSoftwareComponents 60
5.1SwitchtoDaVinciDeveloper 60
5.2DesignSoftwareComponents 61
6STEP6Mappings 62
6.1PerformDataMappingwithinDaVinciDeveloperorDaVinciConfigurator? 62
6.2DataMappingwithintheDaVinciDeveloper 62
6.2.1DataMappingAutomatically-DaVinciDeveloper 62
6.2.2DataMappingManually-DaVinciDeveloper 64
6.2.3DaVinciDeveloper-Saveandclose 66
6.3Switch(back)toDaVinciConfigurator 66
6.4SynchronizeSystemDescription 66
6.5AddComponentConnection 66
6.6Service Mapping 67
6.6.1ServiceMappingviaServiceComponent 67
6.6.2ServiceMapping(overview) 68
6.7AddDataMapping 69
6.8AddMemoryMapping 71
6.9AddTaskMapping 71
6.9.1TaskMappingAssistant 72
6.9.2TaskMapping 73
7STEP7CodeGeneration 75
7.1GenerateSWCTemplatesandContractPhaseHeaders 75
7.2StartCodeGeneration 75
7.3GenerationProcessfinished! 77
©VectorInformatikGmbH Version13.0.1forRelease19 -5-
Content UserManualStartupwithBMWBAC4.x

### Page 6

©VectorInformatikGmbH Version13.0.1forRelease19 -6-
8STEP8AddRunnableCode 78
8.1ComponentTemplate 78
8.2ImplementCode 79
9STEP9Compile, LinkandTestYourProject 80
9.1Finishyourprojectwithcompilingandlinking 80
9.2Noerrorframes?Congratulations,that’sit! 80
IIConcept 81
1General Overview 82
1.1SoftwareComponent 84
1.1.1Atomiccomponents 84
1.1.2Compositions 84
1.2Runnables 84
1.3Ports 85
1.3.1ApplicationPortInterfaces 85
1.3.2ServicePortInterfaces 85
1.4DataElementTypes 85
1.5Connections 85
1.6RTE 86
1.7BSW–BasicSoftwareModules 86
1.8Software,ToolsandFiles 86
1.9StructureoftheSIPFolder 88
2Set-UpNewProject 91
2.1DaVinciConfigurator 91
2.1.1TheMainWindowofDaVinciConfiguratorPro 91
2.1.2EditorsandAssistants 93
3DefineProjectSettings 96
3.1Inputfiles 96
3.1.1SystemDescriptionFiles 96
3.1.2SYSEX 96
3.1.3ECUEX 96
Content UserManualStartupwithBMWBAC4.x

### Page 7

3.1.4LegacyDataBasefiles(DBC,LDF,FIBEX,…) 96
3.1.5DiagnosticDataFiles 97
3.1.6CDD/ODX 97
3.1.7StateDescription 97
3.1.8StandardConfigurationFiles 98
3.2ExternalGenerationSteps 98
3.3ActivateBSW 98
4Validation 99
4.1ValidationConcept 99
5BSW ConfigurationwithConfigurationEditors 100
5.1DaVinciConfiguratorProEditors 100
6SoftwareComponent(SWC)Design 101
6.1DataExchangebetweenDaVinciDeveloperandDaVinciConfiguratorPro 101
6.2AboutApplicationComponents,Ports,Connections,RunnablesandMore… 101
6.3ApplicationComponents 102
6.3.1TheObjectBrowser–Types,PackagesandFiles 102
6.3.2NewApplicationComponents 106
6.3.3UnderstandTypes,PrototypesandInterfaces 110
6.4Ports,PortInitValuesandDataElements 111
6.5ConfigureServicePortswithinyourApplicationComponents 115
6.6DefineyourRunnables 116
6.7TriggersfortheRunnables 117
6.8PortAccessoftheRunnables 119
7Mappings 121
7.1DataMapping 121
7.2TaskMapping 122
7.2.1InformationaboutInteractionbetweenRunnable,Re-entranceandTaskMapping 122
7.3MemoryMapping 125
7.4Service Mapping 126
8Generation 128
©VectorInformatikGmbH Version13.0.1forRelease19 -7-
Content UserManualStartupwithBMWBAC4.x

### Page 8

©VectorInformatikGmbH Version13.0.1forRelease19 -8-
8.1MICROSAR RteGen 128
9RunnableCode 129
10Compile andLink 131
10.1Usingyour"real"hardware 131
IIIAdditionalInformation 132
1UpdateInputFiles 133
1.1SystemDescriptionFiles 133
1.2DiagnosticDataFiles 133
2UpdateProjectSettings 134
3SupportRequestvia DaVinciConfiguratorPro 135
3.1Result 135
4SIP UpdateandProjectMigration 137
4.1Releasex-1toReleasex(necessarystepsforanyupdate) 137
4.2MigrationStepsfromRelease18SIPtoRelease19 139
4.2.1MigrationofDEM 139
4.2.2MemMapHandling 140
4.2.3MigrationofSTBM 140
4.2.4NewDaVinciDeveloperVersion-Workspaceconversionnecessary! 140
4.3MigrationStepsfromRelease17SIPtoRelease18 140
4.4MigrationStepsfromRelease16SIPtoRelease17 140
4.5MigrationStepsfromRelease15SIPtoRelease16 140
4.6MigrationStepstooroverRelease15accordingtoFeature1657 141
4.6.1PDUs 141
4.6.2DEM 141
4.7MigrationStepsRelease12ProjectstoRelease13 141
4.8MigrationStepsfromRelease8toRelease9 143
4.9MigrationStepsfromRelease7toRelease8 143
4.10FirstStepsafterinstallingourMICROSARRelease8SIP 144
4.10.1PreparationsforSIPupdate 144
4.10.2SIPUpdate 144
Content UserManualStartupwithBMWBAC4.x

*Excerpt: first 8 of 217 pages shown.*
