# Electric Power Steering (EPS) System for BMW FAAR WE

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![Language: C](https://img.shields.io/badge/Language-C-blue.svg)](https://en.wikipedia.org/wiki/C_(programming_language))
[![Platform: Renesas RH850](https://img.shields.io/badge/Platform-Renesas_RH850-red.svg)](https://www.renesas.com/rh850)
[![Standard: AUTOSAR](https://img.shields.io/badge/Standard-AUTOSAR-green.svg)](https://www.autosar.org)
[![Safety: ASIL D](https://img.shields.io/badge/Safety-ISO26262_ASIL_D-orange.svg)](https://www.iso.org/standard/43464.html)
[![Documentation](https://img.shields.io/badge/Docs-GitHub_Pages-blueviolet.svg)](docs/)

Complete **Electric Power Steering (EPS)** firmware for the **BMW FAAR WE**
platform, running on a **Renesas RH850/P1x** microcontroller and developed to
**AUTOSAR** and **ISO 26262 ASIL D**.

> **Full documentation:** published to GitHub Pages from [`docs/`](docs/)
> (enable *Settings > Pages > Source: GitHub Actions*; the public URL is
> shown there).

## Table of contents

- [Features](#features)
- [Documentation](#documentation)
- [Repository structure](#repository-structure)
- [AUTOSAR layers](#autosar-layers)
- [Module inventory (layer + origin)](#module-inventory-layer--origin)
- [Installation / build](#installation--build)
- [Contributing](#contributing)
- [License](#license)

## Features

- **Key components**:
  - **Renesas RH850/P1x**: the microcontroller used for EPS control.
  - **AUTOSAR**: the software development standard for automotive embedded systems.
  - **ISO 26262 ASIL D**: the functional safety standard applied to this system.
  - **FlexRay**: real-time communication protocol (see the `Fr*` stack and the
    18 `MM*` message-slot components).
  - **UDS / XCP**: on-board diagnostics (`Dcm`/`Dem`) and calibration (`Xcp`).
- **Functionality**:
  - Precise power-assisted steering control.
  - Electric motor power management.
  - Integration of communication security (cybersecurity).

## Documentation

The documentation site source lives in the **[`docs/`](docs/)** folder (an
Astro + Starlight project). It is published to GitHub Pages on every push to
`main` (see [`.github/workflows/deploy.yml`](.github/workflows/deploy.yml)):

- **Deployed site:** GitHub Pages (see *Settings > Pages* for the public URL).
- **Documentation source:** [`docs/`](docs/) — start there.
- **Build it locally:**

  ```sh
  cd docs
  npm install
  npm run dev   # preview with hot reload
  npm run build # production build into docs/dist/
  ```

The site organises all **211 software modules by AUTOSAR layer**, labels every
module with its **origin** (Vector / BMW / Renesas / Custom), and publishes
searchable excerpts of all **452 Word/PDF documents** found in the repository.

## Repository structure

```text
.                          # EPS firmware sources (C + AUTOSAR artefacts)
├── SF*_*, CF*_*, MM*_*, NM*_*   # Application Software (ASW) — SW-Cs
├── CM*_*, ES*_*, DF*_*, BMW_001A* # Complex Device Drivers (CDD)
├── Com, PduR, NvM, Dem, ...      # Basic Software (BSW) — Vector MICROSAR
├── Rmh, BUtil, Coding, ...       # Basic Software (BSW) — BMW BAC platform
├── Mcu, Port, Dio, Spi, Fls, Wdg # MCAL — Renesas RH850 drivers
├── Rte/  Os/                     # Runtime Environment / Operating System
├── AR*_*, *_GlbPrm_Impl          # Platform libraries
├── TL*                           # Host-side tools (DaVinci, Python, ...)
├── _Bmw_5441_Eps_Impl_A/         # Top-level ECU integration project
├── docs/                         # <-- Documentation site (Astro + Starlight)
│   ├── astro.config.mjs          # Starlight config (site URL auto-derived)
│   ├── package.json
│   └── src/content/docs/         # asw/ cdd/ bsw/ mcal/ rte/ os/ libs/
│                                 # integration/ tools/ general/
├── .github/workflows/            # Pages deploy + Dependabot auto-merge
├── LICENSE                       # MIT License
└── README.md
```

> The rest of the repository (C code, ARXML, tooling) is intentionally
> untouched by the documentation project — only `docs/`, `README.md`,
> `LICENSE` and `.github/` were added.

## AUTOSAR layers

| Layer | Folder | Contents |
| --- | --- | --- |
| Application Software (ASW) | `SF*`, `CF*`, `MM*`, `NM*` | 81 steering, customer, message-slot and manufacturing SW-Cs |
| Complex Device Drivers (CDD) | `CM*`, `ES*`, `DF*`, `BMW_001A` | 56 hardware-near drivers, sensing/actuation, fault injection |
| Basic Software (BSW) | `Com`, `Dem`, `Rmh`, … | 41 Vector MICROSAR + BMW BAC services, ECU abstraction |
| MCAL | `Mcu`, `Port`, … | 8 Renesas RH850 drivers + support |
| RTE / OS | `Rte/`, `Os/` | Vector MICROSAR runtime environment + operating system |
| Platform libraries | `AR*`, `*GlbPrm*` | 12 shared libraries, startup, global parameters |
| ECU integration | `_Bmw_5441_Eps_Impl_A/` | Top-level DaVinci-generated ECU project |
| Tools & support | `TL*`, `*Suprt` | 10 host tool packages and support glue |

### Origin of the code

Third-party code is clearly distinguished from in-house code — on every
documentation page and in the table below:

- **Vector** — Vector Informatik MICROSAR BSW, OS, RTE (28 modules).
- **BMW** — BMW AUTOSAR Core (BAC) platform modules (14 modules).
- **Renesas** — RH850/P1x MCAL drivers (7 modules).
- **Custom** — Nexteer in-house application, drivers, tools, integration
  (162 modules; RTE scaffolding generated with Vector DaVinci tooling).

See the [Vector vs in-house guide](docs/src/content/docs/general/origin-guide.md)
for recognition rules and header evidence.

## Module inventory (layer + origin)

<details>
<summary>Click to expand the full table of all 211 modules</summary>

| Module | Layer | Origin |
| --- | --- | --- |
| `AR099A_McalErrHndlg_Impl` | mcal | Custom |
| `AR100A_NxtrMath_Impl` | libs | Custom |
| `AR101A_NxtrIntrpn_Impl` | libs | Custom |
| `AR102A_NxtrTi_Impl` | libs | Custom |
| `AR103A_NxtrFixdPt_Impl` | libs | Custom |
| `AR104A_NxtrFil_Impl` | libs | Custom |
| `AR200A_ArSuprt_Impl` | libs | Custom |
| `AR201A_ArCplrSuprt_Impl` | libs | Custom |
| `AR202A_MicroCtrlrSuprt_Impl` | libs | Custom |
| `AR300A_MotCtrlMgr_Impl` | libs | Custom |
| `AR400A_NxtrStrtUp_Impl` | libs | Custom |
| `AR998A_NxtrDet_Impl` | libs | Custom |
| `AR999A_ArchGlbPrm_Impl` | libs | Custom |
| `BMW_001A_ChkPt_Impl` | cdd | Custom |
| `BUtil` | bsw | BMW |
| `BmwBacSuprt` | bsw | BMW |
| `BswM` | bsw | Vector |
| `CF011A_BmwTrfcJamAssiDampg_Impl` | asw | Custom |
| `CF020A_BmwHaptcFb_Impl` | asw | Custom |
| `CF040A_BmwTqOvrlCdngAndDrvgDynFac_Impl` | asw | Custom |
| `CF045A_BmwSplyCurrLim_Impl` | asw | Custom |
| `CF069A_BmwStReqMgr_Impl` | asw | Custom |
| `CF070A_BmwFltHndlg_Impl` | asw | Custom |
| `CF071A_BmwHwAgArbnAndEotPosn_Impl` | asw | Custom |
| `CF080A_BmwVehSpd_Impl` | asw | Custom |
| `CF081A_BmwTunSetHndlr_Impl` | asw | Custom |
| `CF082A_BmwPwrPrkgDampg_Impl` | asw | Custom |
| `CF083A_BmwMotTqOvrlArbn_Impl` | asw | Custom |
| `CF084A_BmwDiagcSrvHndlg_Impl` | asw | Custom |
| `CF089A_BmwDrvgDynStMac_Impl` | asw | Custom |
| `CF101A_BmwHwTqOvrlArbn_Impl` | asw | Custom |
| `CF108A_BmwSwFctDi_Impl` | asw | Custom |
| `CM020A_Bmw5441McuCfg_Design` | mcal | Custom |
| `CM101A_ExcpnHndlg_Impl` | cdd | Custom |
| `CM102A_FlsMem_Impl` | cdd | Custom |
| `CM103A_RamMem_Impl` | cdd | Custom |
| `CM104A_EcmOutpAndDiagc_Impl` | cdd | Custom |
| `CM106A_McuCoreCfgAndDiagc_Impl` | cdd | Custom |
| `CM107A_GuardCfgAndDiagc_Impl` | cdd | Custom |
| `CM108A_DataAndAdrPar_Impl` | cdd | Custom |
| `CM111A_VrfyCritReg_Impl` | cdd | Custom |
| `CM112A_CoreVltgMonr_Impl` | cdd | Custom |
| `CM200B_DmaCfgAndUse_Impl` | cdd | Custom |
| `CM300A_Adc0CfgAndUse_Impl` | cdd | Custom |
| `CM320A_Adc1CfgAndUse_Impl` | cdd | Custom |
| `CM340A_AdcDiagc_Impl` | cdd | Custom |
| `CM455A_Tauj0CfgAndUse_Impl` | cdd | Custom |
| `CM475A_TSG31CfgAndUse_Impl` | cdd | Custom |
| `CM510A_MotAg3Meas_Impl` | cdd | Custom |
| `CM515A_MotAg4Meas_Impl` | cdd | Custom |
| `CM620B_MotAg0Meas_Impl` | cdd | Custom |
| `CM640B_MotAg1Meas_Impl` | cdd | Custom |
| `CM800A_SyncCrc_Impl` | cdd | Custom |
| `Coding` | bsw | BMW |
| `ComM` | bsw | Vector |
| `Com` | bsw | Vector |
| `Crc` | bsw | Vector |
| `Crypto` | bsw | BMW |
| `DF001A_FltInj_Impl` | cdd | Custom |
| `DF002A_Swp_Impl` | cdd | Custom |
| `DF003A_McuErrInj_Impl` | cdd | Custom |
| `Darh` | bsw | BMW |
| `Dcm` | bsw | Vector |
| `Dem` | bsw | Vector |
| `Det` | bsw | Vector |
| `Dio` | mcal | Renesas |
| `DlogShared` | bsw | BMW |
| `Dlog` | bsw | BMW |
| `E2EPW` | bsw | Vector |
| `E2E` | bsw | Vector |
| `ES002A_McuDiagc_Impl` | cdd | Custom |
| `ES003B_PwrDiscnct_Impl` | cdd | Custom |
| `ES004A_PwrUpSeq_Impl` | cdd | Custom |
| `ES005C_TmplMonr_Impl` | cdd | Custom |
| `ES006A_NvM_Impl` | cdd | Custom |
| `ES008A_PwrSply_Impl` | cdd | Custom |
| `ES100A_SysStMod_Impl` | cdd | Custom |
| `ES101A_DiagcMgr_Impl` | cdd | Custom |
| `ES102A_PolarityCfg_Impl` | cdd | Custom |
| `ES104B_XcpIf_Impl` | cdd | Custom |
| `ES108A_ShtdwnMech_Impl` | cdd | Custom |
| `ES200B_CurrMeas_Impl` | cdd | Custom |
| `ES208A_CurrMeasArbn_Impl` | cdd | Custom |
| `ES209B_CurrMeasCorrln_Impl` | cdd | Custom |
| `ES210A_EcuTMeas_Impl` | cdd | Custom |
| `ES220A_HwTq4Meas_Impl` | cdd | Custom |
| `ES221A_HwTq5Meas_Impl` | cdd | Custom |
| `ES228B_HwTqArbn_Impl` | cdd | Custom |
| `ES229B_HwTqCorrln_Impl` | cdd | Custom |
| `ES247A_MotAgCmp_Impl` | cdd | Custom |
| `ES249B_MotAgCorrln_Impl` | cdd | Custom |
| `ES250B_BattVltg_Impl` | cdd | Custom |
| `ES251A_BattRtnCurr_Impl` | cdd | Custom |
| `ES252A_RvsBattProtn_Impl` | cdd | Custom |
| `ES259B_BattVltgCorrln_Impl` | cdd | Custom |
| `ES261A_TurnCntrCorrln_Impl` | cdd | Custom |
| `ES300A_SinVltgGenn_Impl` | cdd | Custom |
| `ES311A_GateDrv0Ctrl_Impl` | cdd | Custom |
| `ES330A_PhaDiscnct_Impl` | cdd | Custom |
| `ES340A_SerlComTrcvIf_Impl` | cdd | Custom |
| `ES400A_TunSelnMngt_Impl` | cdd | Custom |
| `ES999A_ElecGlbPrm_Impl` | cdd | Custom |
| `EcuC` | bsw | Vector |
| `EcuM` | bsw | Vector |
| `Fee_30_SmallSector` | bsw | Vector |
| `Fls` | bsw | Renesas |
| `FrIf` | bsw | Vector |
| `FrSM` | bsw | Vector |
| `FrTp` | bsw | Vector |
| `FrTrcv_30_Tja1082` | bsw | Vector |
| `FrXcp` | bsw | Vector |
| `Fr` | bsw | Vector |
| `IoHwAb` | bsw | Vector |
| `IpduM` | bsw | Vector |
| `MM096A_BmwMsgSlot53Bas3Repn8BusFrChA_Impl` | asw | Custom |
| `MM097A_BmwMsgSlot55Bas0Repn2BusFrChA_Impl` | asw | Custom |
| `MM098A_BmwMsgSlot55Bas3Repn4BusFrChA_Impl` | asw | Custom |
| `MM099A_BmwMsgSlot56Bas0Repn2BusFrChA_Impl` | asw | Custom |
| `MM101A_BmwMsgSlot68Bas0Repn2BusFrChA_Impl` | asw | Custom |
| `MM102A_BmwMsgSlot68Bas1Repn2BusFrChA_Impl` | asw | Custom |
| `MM105A_BmwMsgSlot107Bas0Repn1BusFrChA_Impl` | asw | Custom |
| `MM106A_BmwMsgSlot108Bas0Repn2BusFrChA_Impl` | asw | Custom |
| `MM109A_BmwMsgSlot121Bas1Repn2BusFrChA_Impl` | asw | Custom |
| `MM118A_BmwMsgSlot269Bas2Repn4BusFrChA_Impl` | asw | Custom |
| `MM122A_BmwMsgSlot276Bas4Repn8BusFrChA_Impl` | asw | Custom |
| `MM521A_BmwMsgSlot49Bas0Repn2BusFrChA_Impl` | asw | Custom |
| `MM522A_BmwMsgSlot49Bas1Repn2BusFrChA_Impl` | asw | Custom |
| `MM523A_BmwMsgSlot51Bas0Repn2BusFrChA_Impl` | asw | Custom |
| `MM526A_BmwMsgSlot234Bas1Repn2BusFrChA_Impl` | asw | Custom |
| `MM528A_BmwMsgSlot274Bas0Repn8BusFrChA_Impl` | asw | Custom |
| `MM529A_BmwMsgSlot274Bas2Repn4BusFrChA_Impl` | asw | Custom |
| `MM530A_BmwMsgSlot315Bas0Repn1BusFrChA_Impl` | asw | Custom |
| `Mcu` | mcal | Renesas |
| `MemIf` | bsw | Vector |
| `NM001A_CmnMfgSrv_Impl` | asw | Custom |
| `NM002C_CmnMfgSrvIf_Impl` | asw | Custom |
| `NM003A_NxtrSwIds_Impl` | asw | Custom |
| `NM004A_NxtrCalIds_Impl` | asw | Custom |
| `NM010B_ProgMfgSrv_Impl` | asw | Custom |
| `NM100A_MotVelCtrl_Impl` | asw | Custom |
| `NvM` | bsw | Vector |
| `Omc` | bsw | BMW |
| `Os` | os | Vector |
| `PduR` | bsw | Vector |
| `Port` | mcal | Renesas |
| `RenesasMcalSuprt` | mcal | Renesas |
| `Rmh` | bsw | BMW |
| `Rte` | rte | Vector |
| `SF005A_StOutpCtrl_Impl` | asw | Custom |
| `SF006A_TEstimn_Impl` | asw | Custom |
| `SF007A_SysFricLrng_Impl` | asw | Custom |
| `SF009A_DutyCycThermProtn_Impl` | asw | Custom |
| `SF013A_PullCmpActv_Impl` | asw | Custom |
| `SF014A_InertiaCmpVel_Impl` | asw | Custom |
| `SF016A_VehSpdLimr_Impl` | asw | Custom |
| `SF017A_HiLoadStallLimr_Impl` | asw | Custom |
| `SF018A_EotProtn_Impl` | asw | Custom |
| `SF019D_PwrLimr_Impl` | asw | Custom |
| `SF020B_PosnTrakgServo_Impl` | asw | Custom |
| `SF023A_TunSelnAuthy_Impl` | asw | Custom |
| `SF024A_LrnPinionCentr_Impl` | asw | Custom |
| `SF032A_MotTqCmdSca_Impl` | asw | Custom |
| `SF033A_VehSigCdng_Impl` | asw | Custom |
| `SF038A_LimrCdng_Impl` | asw | Custom |
| `SF039A_LrndRackCentr_Impl` | asw | Custom |
| `SF040A_MotVel_Impl` | asw | Custom |
| `SF041A_CmplncErr_Impl` | asw | Custom |
| `SF043A_TqOscn_Impl` | asw | Custom |
| `SF049B_LoaMgr_Impl` | asw | Custom |
| `SF050A_MotTqTranlDampg_Impl` | asw | Custom |
| `SF065A_CtrldVelRtn_Impl` | asw | Custom |
| `SF066A_EpsStEstimn_Impl` | asw | Custom |
| `SF067A_MotTqCalcd_Impl` | asw | Custom |
| `SF068A_Effort_Impl` | asw | Custom |
| `SF069A_HwRefTqSum_Impl` | asw | Custom |
| `SF070A_HwTqTrakgCtrl_Impl` | asw | Custom |
| `SF071A_SysKineAndEff_Impl` | asw | Custom |
| `SF072A_ClsdLoopDampg_Impl` | asw | Custom |
| `SF073A_ClsdLoopHys_Impl` | asw | Custom |
| `SF101A_MotQuadDetn_Impl` | asw | Custom |
| `SF102A_MotCtrlPrmEstimn_Impl` | asw | Custom |
| `SF103A_MotRefMdl_Impl` | asw | Custom |
| `SF104A_MotCurrRegCfg_Impl` | asw | Custom |
| `SF105A_MotCurrRegVltgLimr_Impl` | asw | Custom |
| `SF108A_MotCurrPeakEstimn_Impl` | asw | Custom |
| `SF109A_ElecPwrCns_Impl` | asw | Custom |
| `SF110A_GlbLimr_Impl` | asw | Custom |
| `SF111A_FalbckAssi_Impl` | asw | Custom |
| `SF112A_SteerCmdArbnAndLim_Impl` | asw | Custom |
| `SF999A_SysGlbPrm_Impl` | asw | Custom |
| `Spi` | mcal | Renesas |
| `Srv` | bsw | BMW |
| `StdDiag` | bsw | BMW |
| `Stm` | bsw | BMW |
| `SysTime` | bsw | BMW |
| `TL102A_Davinci` | tools | Custom |
| `TL105A_Artt` | tools | Custom |
| `TL109A_SwcSuprt` | tools | Custom |
| `TL111A_CmnChksTool` | tools | Custom |
| `TL112A_Python` | tools | Custom |
| `TL113A_MfgSrvSuprt` | tools | Custom |
| `TL117A_DataDict` | tools | Custom |
| `TL119A_Python3` | tools | Custom |
| `TL125A_PAGe` | tools | Custom |
| `VectorBswSuprt` | tools | Custom |
| `Vin` | bsw | BMW |
| `WdgIf` | bsw | Vector |
| `WdgM` | bsw | Vector |
| `Wdg` | mcal | Renesas |
| `Xcp` | bsw | Vector |
| `_Bmw_5441_Eps_Impl_A` | integration | Custom |
</details>

## Installation / build

1. Clone this repository:

   ```sh
   git clone <repository-url>
   cd <repository-directory>
   ```

2. Install the licensed toolchains (Vector DaVinci, Green Hills for RH850).
   These are not versioned here; see the
   [build-system documentation](docs/src/content/docs/general/build-system.md)
   for the generation flow (`DaVinci → generate/ → make/CMake → link`).
3. Run generation, compile, link and flash the image onto the Renesas RH850
   microcontroller.

To work on this documentation only, all you need is Node.js ≥ 22.12 (Astro 7 requirement; CI uses Node 22):

```sh
cd docs && npm install && npm run dev
```

## BMW FAAR WE Platform

The **BMW FAAR WE** platform is an advanced electronic architecture for BMW
vehicles. It offers cutting-edge features, extended connectivity, and enhanced
security.

## Contributing

We encourage contributions! If you'd like to improve this project, please
submit a pull request. Documentation-only changes live under [`docs/`](docs/)
and are previewed automatically on pull requests touching that folder.

## License

This project is licensed under the MIT License — see the [LICENSE](LICENSE)
file for the full text.

> **Third-party note:** files carrying their own proprietary headers
> (Vector Informatik, BMW AG, Renesas, Nexteer) remain governed by those
> headers; the MIT license covers the documentation and glue added by this
> project and does not override the in-file notices of third-party sources.
