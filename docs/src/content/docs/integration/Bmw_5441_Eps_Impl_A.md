---
title: '_Bmw_5441_Eps_Impl_A ECU project'
description: 'Top-level ECU integration project for the BMW 5441 EPS (generated configuration, callout stubs, memory mapping).'
---

:::tip[Origin: Custom · ECU integration project]
Top-level integration: Nexteer application + BMW BAC + Vector MICROSAR configuration + Renesas MCAL, generated with DaVinci Configurator.
File scaffolding in this module was generated with the Vector MICROSAR RTE Generator (DaVinci tooling); the application logic itself is in-house.
:::

## Purpose

Top-level ECU integration project for the BMW 5441 EPS controller: DaVinci-generated
BSW/RTE configuration (`generate/`), BSW callout stubs (`*_Callout_Stubs.c`, `DemWrapper.c`),
memory-mapping headers (`*_MemMap.h`, `Compiler_Cfg.h`), DTC mapping and calibration dummies.
It binds the application SW-Cs, BMW BAC modules, Vector MICROSAR BSW and Renesas MCAL
into one buildable ECU image.

> **Naming note:** the repository directory is `_Bmw_5441_Eps_Impl_A/`. The documentation
> page is named `Bmw_5441_Eps_Impl_A` (without the leading underscore) because Astro
> ignores content files starting with `_`.

*Repository path:* `_Bmw_5441_Eps_Impl_A/` · *AUTOSAR layer:* [ECU Integration](../) · *Implementation tag:* `Impl (implementation package)`

*Classification evidence (header scan of `*.c`/`*.h`):* bmw: 75 file(s), gen: 1250 file(s), nexteer: 1502 file(s), renesas: 221 file(s), vector: 1283 file(s).

## Key files

| Area | Files |
| --- | --- |
| `src/` (16 C file(s)) | `BacComIf.c`, `BswM_Callout_Stubs.c`, `CDD_Bmw5441McuCfg_Stub.c`, `CalDummy_Stub.c`, `DTCMapping.c`, `Dcm_Callout_Stubs.c`, `DemWrapper.c`, `DiagcMgr.c`, `E2EPW_Init.c`, `EcuM_Callout_Stubs.c`, `FrTrcv_Callout_Stubs.c`, `Fr_Callout_Stubs.c` |
| `include/` (29 header(s)) | `BUtil_MemMap.h`, `BswM_UserTypes.h`, `CDD_Bmw5441McuCfg_Stub.h`, `CDD_HwTq4Meas_Cfg.h`, `CDD_HwTq5Meas_Cfg.h`, `Coding_MemMap.h`, `Compiler_Cfg.h`, `Crypto_Keys.h`, `Crypto_MemMap.h`, `DTCMapping.h`, `Darh_MemMap.h`, `Dlog_MemMap.h` |
| `autosar/` (0 ARXML) | — |
| Build/config | `generate/` (DaVinci), `tools/` |
| Review artefacts | 13 spreadsheet checklist(s) (`*.xls*`, not converted) |

## Public API (excerpt)

Detected `FUNC(...)` entry points in headers/sources (first 15):

- `BswMUser_GetDtcFailed`
- `Bmw5441McuCfgPer1`
- `Adc0OutpInin`
- `VehicleState`
- `VinUpdate`
- `BswM_SHUTDOWN_NvMWriteAll`
- `BswM_FinalizeShtdwn`
- `BswM_INIT_NvMReadAll`
- `BswM_ShtdwnHndlg_PrepShutdown`
- `BswM_Restart`
- `BswM_DiagcMgrPwrDwn`
- `BwmM_GetShutdownOngoing`
- `BswM_AL_SetProgrammableInterrupts`
- `Bmw5441McuCfgInit1`
- `Bmw5441McuCfgInit2`

Typical lifecycle: `…_Init` → runnables / cyclic processing → `…_GetVersionInfo` / `…_DeInit` where applicable.

## Dependencies (excerpt)

Direct quoted includes found in `src/*.c` (first 15):

- `Rte_BacComIf.h`
- `BacComIf_MemMap.h`
- `BswM.h`
- `BswM_Private_Cfg.h`
- `WdgM.h`
- `WdgM_PBcfg.h`
- `WdgIf.h`
- `Os.h`
- `CDD_NvMProxy.h`
- `CDD_NvMProxy_Cbk.h`
- `CDD_ExcpnHndlg.h`
- `DiagcMgr.h`
- `CDD_NxtrTi.h`
- `Wdgm_PBcfg.h`
- `MemMap.h`

## Documents

Converted from the module `doc/` folder (Word/PDF → Markdown excerpts):

- [DVCfg_AutomationInterfaceDocumentation](../bmw_5441_eps_impl_a__dvcfg-automationinterfacedocumentation-pdf/)
- [AN-ISC-8-1140_FrIf_JobListConfiguration](../bmw_5441_eps_impl_a__an-isc-8-1140-frif-joblistconfiguration-pdf/)
- [AN-ISC-8-1153_ThirdPartyModules](../bmw_5441_eps_impl_a__an-isc-8-1153-thirdpartymodules-pdf/)
- [AN-ISC-8-1166_RTE_BRE_without_AUTOSAR_OS](../bmw_5441_eps_impl_a__an-isc-8-1166-rte-bre-without-autosar-os-pdf/)
- [AN-ISC-8-1170_Use_AR3_SWCs_in_AR4](../bmw_5441_eps_impl_a__an-isc-8-1170-use-ar3-swcs-in-ar4-pdf/)
- [AN-ISC-8-1184_Compiler_Warnings](../bmw_5441_eps_impl_a__an-isc-8-1184-compiler-warnings-pdf/)
- [AN-ISC-8-1196_Distributing_BSW_Components_across_Partitions](../bmw_5441_eps_impl_a__an-isc-8-1196-distributing-bsw-components-across-partitions-pdf/)
- [AN-ISC-8-1207_Synchronization_Cry_Fls](../bmw_5441_eps_impl_a__an-isc-8-1207-synchronization-cry-fls-pdf/)
- [AN-ISC-8-1208_DaVinciTeamAndPlatformSupport](../bmw_5441_eps_impl_a__an-isc-8-1208-davinciteamandplatformsupport-pdf/)
- [AN-ISC-8-1211_Limitations_of_MICROSAR_RTE_for_Partition_Termination](../bmw_5441_eps_impl_a__an-isc-8-1211-limitations-of-microsar-rte-for-partition-termination-pdf/)
- [AN-ISC-8-1213_Compliance Documentation MISRA-C_2004](../bmw_5441_eps_impl_a__an-isc-8-1213-compliance-documentation-misra-c-2004-pdf/)
- [2659.0_NS_LUA_Nexteer_MSR_Bmw_SLP4_RH850-CBD1700369.D00](../bmw_5441_eps_impl_a__2659-0-ns-lua-nexteer-msr-bmw-slp4-rh850-cbd1700369-d00-pdf/)
- [IssueReport_CBD1700369](../bmw_5441_eps_impl_a__issuereport-cbd1700369-pdf/)
- [ProductInformation_2_MICROSAR4](../bmw_5441_eps_impl_a__productinformation-2-microsar4-pdf/)
- [ProductInformation_2_MSR4-MICROSARSafe](../bmw_5441_eps_impl_a__productinformation-2-msr4-microsarsafe-pdf/)
- [Readme_CBD1700369_D04](../bmw_5441_eps_impl_a__readme-cbd1700369-d04-pdf/)
- [ReleaseNotes_3rdPartyMCAL_VectorIntegration](../bmw_5441_eps_impl_a__releasenotes-3rdpartymcal-vectorintegration-pdf/)
- [Safety_Manual_CBD1700369_D04](../bmw_5441_eps_impl_a__safety-manual-cbd1700369-d04-pdf/)
- [Startup_BMW_BAC40](../bmw_5441_eps_impl_a__startup-bmw-bac40-pdf/)
- [ReferenceManual_HexView](../bmw_5441_eps_impl_a__referencemanual-hexview-pdf/)
- [TechnicalReference_3rdParty-MCAL-Integration](../bmw_5441_eps_impl_a__technicalreference-3rdparty-mcal-integration-pdf/)
- [TechnicalReference_Asr_FrTp](../bmw_5441_eps_impl_a__technicalreference-asr-frtp-pdf/)
- [TechnicalReference_Asr_MemoryMapping](../bmw_5441_eps_impl_a__technicalreference-asr-memorymapping-pdf/)
- [TechnicalReference_BswM](../bmw_5441_eps_impl_a__technicalreference-bswm-pdf/)
- [TechnicalReference_Cal](../bmw_5441_eps_impl_a__technicalreference-cal-pdf/)
- [TechnicalReference_Cdd_Communication](../bmw_5441_eps_impl_a__technicalreference-cdd-communication-pdf/)
- [TechnicalReference_Com](../bmw_5441_eps_impl_a__technicalreference-com-pdf/)
- [TechnicalReference_ComM](../bmw_5441_eps_impl_a__technicalreference-comm-pdf/)
- [TechnicalReference_ComStackLib](../bmw_5441_eps_impl_a__technicalreference-comstacklib-pdf/)
- [TechnicalReference_ComXf](../bmw_5441_eps_impl_a__technicalreference-comxf-pdf/)
- [TechnicalReference_Crc](../bmw_5441_eps_impl_a__technicalreference-crc-pdf/)
- [TechnicalReference_CryIf](../bmw_5441_eps_impl_a__technicalreference-cryif-pdf/)
- [TechnicalReference_Cry_30_Rh850Icus](../bmw_5441_eps_impl_a__technicalreference-cry-30-rh850icus-pdf/)
- [TechnicalReference_Crypto_30_CryWrapper](../bmw_5441_eps_impl_a__technicalreference-crypto-30-crywrapper-pdf/)
- [TechnicalReference_Csm](../bmw_5441_eps_impl_a__technicalreference-csm-pdf/)
- [TechnicalReference_DaVinciConfigurator_Licenses](../bmw_5441_eps_impl_a__technicalreference-davinciconfigurator-licenses-pdf/)
- [TechnicalReference_Det](../bmw_5441_eps_impl_a__technicalreference-det-pdf/)
- [TechnicalReference_DiagA2lGen](../bmw_5441_eps_impl_a__technicalreference-diaga2lgen-pdf/)
- [TechnicalReference_E2E](../bmw_5441_eps_impl_a__technicalreference-e2e-pdf/)
- [TechnicalReference_E2EXf](../bmw_5441_eps_impl_a__technicalreference-e2exf-pdf/)
- [TechnicalReference_EcuM](../bmw_5441_eps_impl_a__technicalreference-ecum-pdf/)
- [TechnicalReference_Fee_30_SmallSector](../bmw_5441_eps_impl_a__technicalreference-fee-30-smallsector-pdf/)
- [TechnicalReference_Fr](../bmw_5441_eps_impl_a__technicalreference-fr-pdf/)
- [TechnicalReference_FrIf](../bmw_5441_eps_impl_a__technicalreference-frif-pdf/)
- [TechnicalReference_FrSM](../bmw_5441_eps_impl_a__technicalreference-frsm-pdf/)
- [TechnicalReference_FrTrcv_Tja1082](../bmw_5441_eps_impl_a__technicalreference-frtrcv-tja1082-pdf/)
- [TechnicalReference_FrXcp](../bmw_5441_eps_impl_a__technicalreference-frxcp-pdf/)
- [TechnicalReference_Fr_V85x](../bmw_5441_eps_impl_a__technicalreference-fr-v85x-pdf/)
- [TechnicalReference_GenTool_CsAsrLegacyDb2SystemDescr_Vector](../bmw_5441_eps_impl_a__technicalreference-gentool-csasrlegacydb2systemdescr-vector-pdf/)
- [TechnicalReference_IoHwAb](../bmw_5441_eps_impl_a__technicalreference-iohwab-pdf/)
- [TechnicalReference_IpduM](../bmw_5441_eps_impl_a__technicalreference-ipdum-pdf/)
- [TechnicalReference_MSSV](../bmw_5441_eps_impl_a__technicalreference-mssv-pdf/)
- [TechnicalReference_MemIf](../bmw_5441_eps_impl_a__technicalreference-memif-pdf/)
- [TechnicalReference_NvM](../bmw_5441_eps_impl_a__technicalreference-nvm-pdf/)
- [TechnicalReference_Os](../bmw_5441_eps_impl_a__technicalreference-os-pdf/)
- [TechnicalReference_PduR](../bmw_5441_eps_impl_a__technicalreference-pdur-pdf/)
- [TechnicalReference_Rte](../bmw_5441_eps_impl_a__technicalreference-rte-pdf/)
- [TechnicalReference_RteAnalyzer](../bmw_5441_eps_impl_a__technicalreference-rteanalyzer-pdf/)
- [TechnicalReference_SecOC](../bmw_5441_eps_impl_a__technicalreference-secoc-pdf/)
- [TechnicalReference_SipModificationChecker](../bmw_5441_eps_impl_a__technicalreference-sipmodificationchecker-pdf/)
- [TechnicalReference_VStdLib_GenericAsr](../bmw_5441_eps_impl_a__technicalreference-vstdlib-genericasr-pdf/)
- [TechnicalReference_WdgIf](../bmw_5441_eps_impl_a__technicalreference-wdgif-pdf/)
- [TechnicalReference_WdgM](../bmw_5441_eps_impl_a__technicalreference-wdgm-pdf/)
- [TechnicalReference_XCP](../bmw_5441_eps_impl_a__technicalreference-xcp-pdf/)
- [UserManual_AUTOSAR_Calibration](../bmw_5441_eps_impl_a__usermanual-autosar-calibration-pdf/)
- [UserManual_E2EPW](../bmw_5441_eps_impl_a__usermanual-e2epw-pdf/)
- [XCP_ReferenceBook_V3.0_EN](../bmw_5441_eps_impl_a__xcp-referencebook-v3-0-en-pdf/)
- [DocumentationGuide_VectorAUTOSAR](../bmw_5441_eps_impl_a__documentationguide-vectorautosar-pdf/)

Source files remain in the repository next to this documentation.

