---
title: 'Crypto Crypto'
description: 'Crypto (BSW). BMW Crypto library (BAC cryptographic services).'
---

:::note[Origin: BMW-provided · BAC (BMW AUTOSAR Core)]
:::

## Purpose

BMW Crypto library (BAC cryptographic services).

*Repository path:* `Crypto/` · *AUTOSAR layer:* [Basic Software (BSW)](../) · *Implementation tag:* `Impl (implementation package)`

*Classification evidence (header scan of `*.c`/`*.h`):* bmw: 67 file(s).

## Key files

| Area | Files |
| --- | --- |
| `src/` (49 C file(s)) | `Crypto_CertificateHandling.c`, `Crypto_ECDSA.c`, `Crypto_EccOperations.c`, `Crypto_HashDescriptor.c`, `Crypto_Keys.c`, `Crypto_RSA.c`, `Crypto_SHA256.c`, `Crypto_SHA384.c`, `Crypto_SHA512.c`, `fp_2expt.c`, `fp_add.c`, `fp_cmp.c` |
| `include/` (18 header(s)) | `Crypto.h`, `Crypto_BitOperations.h`, `Crypto_Certificate.h`, `Crypto_Certificate_Intern.h`, `Crypto_Common.h`, `Crypto_Common_Intern.h`, `Crypto_ECDSA.h`, `Crypto_ECDSA_Intern.h`, `Crypto_Hash.h`, `Crypto_KeyManagement.h`, `Crypto_KeyManagement_Intern.h`, `Crypto_Math_Intern.h` |
| `autosar/` (2 ARXML) | `CryptoClassic_paramdef.arxml`, `Crypto_paramdef.arxml` |
| Build/config | `make/*.mak`, `tools/` |
| Review artefacts | 1 spreadsheet checklist(s) (`*.xls*`, not converted) |

## Public API (excerpt)

No `FUNC(...)` AUTOSAR-style entry points were detected in the scanned headers (the module may expose RTE ports, generated interfaces, or data tables instead). See the key files above and the design documents below.

## Dependencies (excerpt)

Direct quoted includes found in `src/*.c` (first 13):

- `Crypto_Certificate_Intern.h`
- `Crypto_Version.h`
- `Crypto_MemMap.h`
- `Crypto_ECDSA_Intern.h`
- `Crypto_KeyManagement_Intern.h`
- `Crypto_Common_Intern.h`
- `Crypto_Hash.h`
- `Crypto_Keys.h`
- `Crypto_RSA_Intern.h`
- `Crypto_BitOperations.h`
- `BUtil_ByteMask.h`
- `BUtil_Algorithm.h`
- `string.h`

## Documents

Converted from the module `doc/` folder (Word/PDF → Markdown excerpts):

- [CryptoClassic_IntegrationManual](../crypto__cryptoclassic-integrationmanual-pdf/)
- [CryptoClassic_ReleaseNotes](../crypto__cryptoclassic-releasenotes-pdf/)
- [CryptoGeneric_ReleaseNotes](../crypto__cryptogeneric-releasenotes-pdf/)
- [CryptoGeneric_RequirementsTable](../crypto__cryptogeneric-requirementstable-pdf/)

Source files remain in the repository next to this documentation.

