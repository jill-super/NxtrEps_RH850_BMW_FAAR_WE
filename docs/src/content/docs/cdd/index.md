---
title: 'Complex Device Drivers (CDD)'
description: 'Hardware-near drivers: MCU/ADC/DMA/motor-angle (CM*), EPS sensing and actuation (ES*), fault injection (DF*), checkpoints.'
sidebar:
  order: 0
---

Hardware-near drivers: MCU/ADC/DMA/motor-angle (CM*), EPS sensing and actuation (ES*), fault injection (DF*), checkpoints.

This section contains **56** module(s).

| Module | Origin | Docs |
| --- | --- | --- |
| [BMW_001A_ChkPt_Impl](./bmw_001a_chkpt_impl/) | Custom | 1 |
| [CM101A_ExcpnHndlg_Impl](./cm101a_excpnhndlg_impl/) | Custom | 2 |
| [CM102A_FlsMem_Impl](./cm102a_flsmem_impl/) | Custom | 2 |
| [CM103A_RamMem_Impl](./cm103a_rammem_impl/) | Custom | 2 |
| [CM104A_EcmOutpAndDiagc_Impl](./cm104a_ecmoutpanddiagc_impl/) | Custom | 2 |
| [CM106A_McuCoreCfgAndDiagc_Impl](./cm106a_mcucorecfganddiagc_impl/) | Custom | 2 |
| [CM107A_GuardCfgAndDiagc_Impl](./cm107a_guardcfganddiagc_impl/) | Custom | 2 |
| [CM108A_DataAndAdrPar_Impl](./cm108a_dataandadrpar_impl/) | Custom | 2 |
| [CM111A_VrfyCritReg_Impl](./cm111a_vrfycritreg_impl/) | Custom | 2 |
| [CM112A_CoreVltgMonr_Impl](./cm112a_corevltgmonr_impl/) | Custom | 2 |
| [CM200B_DmaCfgAndUse_Impl](./cm200b_dmacfganduse_impl/) | Custom | 2 |
| [CM300A_Adc0CfgAndUse_Impl](./cm300a_adc0cfganduse_impl/) | Custom | 2 |
| [CM320A_Adc1CfgAndUse_Impl](./cm320a_adc1cfganduse_impl/) | Custom | 2 |
| [CM340A_AdcDiagc_Impl](./cm340a_adcdiagc_impl/) | Custom | 2 |
| [CM455A_Tauj0CfgAndUse_Impl](./cm455a_tauj0cfganduse_impl/) | Custom | 2 |
| [CM475A_TSG31CfgAndUse_Impl](./cm475a_tsg31cfganduse_impl/) | Custom | 2 |
| [CM510A_MotAg3Meas_Impl](./cm510a_motag3meas_impl/) | Custom | 2 |
| [CM515A_MotAg4Meas_Impl](./cm515a_motag4meas_impl/) | Custom | 2 |
| [CM620B_MotAg0Meas_Impl](./cm620b_motag0meas_impl/) | Custom | 2 |
| [CM640B_MotAg1Meas_Impl](./cm640b_motag1meas_impl/) | Custom | 2 |
| [CM800A_SyncCrc_Impl](./cm800a_synccrc_impl/) | Custom | 2 |
| [DF001A_FltInj_Impl](./df001a_fltinj_impl/) | Custom | 2 |
| [DF002A_Swp_Impl](./df002a_swp_impl/) | Custom | 2 |
| [DF003A_McuErrInj_Impl](./df003a_mcuerrinj_impl/) | Custom | 2 |
| [ES002A_McuDiagc_Impl](./es002a_mcudiagc_impl/) | Custom | 2 |
| [ES003B_PwrDiscnct_Impl](./es003b_pwrdiscnct_impl/) | Custom | 2 |
| [ES004A_PwrUpSeq_Impl](./es004a_pwrupseq_impl/) | Custom | 2 |
| [ES005C_TmplMonr_Impl](./es005c_tmplmonr_impl/) | Custom | 2 |
| [ES006A_NvM_Impl](./es006a_nvm_impl/) | Custom | 1 |
| [ES008A_PwrSply_Impl](./es008a_pwrsply_impl/) | Custom | 2 |
| [ES100A_SysStMod_Impl](./es100a_sysstmod_impl/) | Custom | 2 |
| [ES101A_DiagcMgr_Impl](./es101a_diagcmgr_impl/) | Custom | 3 |
| [ES102A_PolarityCfg_Impl](./es102a_polaritycfg_impl/) | Custom | 2 |
| [ES104B_XcpIf_Impl](./es104b_xcpif_impl/) | Custom | 1 |
| [ES108A_ShtdwnMech_Impl](./es108a_shtdwnmech_impl/) | Custom | 2 |
| [ES200B_CurrMeas_Impl](./es200b_currmeas_impl/) | Custom | 2 |
| [ES208A_CurrMeasArbn_Impl](./es208a_currmeasarbn_impl/) | Custom | 2 |
| [ES209B_CurrMeasCorrln_Impl](./es209b_currmeascorrln_impl/) | Custom | 2 |
| [ES210A_EcuTMeas_Impl](./es210a_ecutmeas_impl/) | Custom | 2 |
| [ES220A_HwTq4Meas_Impl](./es220a_hwtq4meas_impl/) | Custom | 2 |
| [ES221A_HwTq5Meas_Impl](./es221a_hwtq5meas_impl/) | Custom | 2 |
| [ES228B_HwTqArbn_Impl](./es228b_hwtqarbn_impl/) | Custom | 2 |
| [ES229B_HwTqCorrln_Impl](./es229b_hwtqcorrln_impl/) | Custom | 2 |
| [ES247A_MotAgCmp_Impl](./es247a_motagcmp_impl/) | Custom | 2 |
| [ES249B_MotAgCorrln_Impl](./es249b_motagcorrln_impl/) | Custom | 2 |
| [ES250B_BattVltg_Impl](./es250b_battvltg_impl/) | Custom | 2 |
| [ES251A_BattRtnCurr_Impl](./es251a_battrtncurr_impl/) | Custom | 2 |
| [ES252A_RvsBattProtn_Impl](./es252a_rvsbattprotn_impl/) | Custom | 2 |
| [ES259B_BattVltgCorrln_Impl](./es259b_battvltgcorrln_impl/) | Custom | 2 |
| [ES261A_TurnCntrCorrln_Impl](./es261a_turncntrcorrln_impl/) | Custom | 2 |
| [ES300A_SinVltgGenn_Impl](./es300a_sinvltggenn_impl/) | Custom | 2 |
| [ES311A_GateDrv0Ctrl_Impl](./es311a_gatedrv0ctrl_impl/) | Custom | 2 |
| [ES330A_PhaDiscnct_Impl](./es330a_phadiscnct_impl/) | Custom | 2 |
| [ES340A_SerlComTrcvIf_Impl](./es340a_serlcomtrcvif_impl/) | Custom | 2 |
| [ES400A_TunSelnMngt_Impl](./es400a_tunselnmngt_impl/) | Custom | 2 |
| [ES999A_ElecGlbPrm_Impl](./es999a_elecglbprm_impl/) | Custom | 2 |

