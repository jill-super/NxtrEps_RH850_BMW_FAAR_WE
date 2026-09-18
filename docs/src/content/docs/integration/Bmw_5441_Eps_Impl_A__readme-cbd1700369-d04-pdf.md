---
title: '_Bmw_5441_Eps_Impl_A — Readme_CBD1700369_D04'
description: 'Converted PDF document Readme_CBD1700369_D04.pdf from module _Bmw_5441_Eps_Impl_A.'
sidebar:
  hidden: true
---

> **Source:** `Readme_CBD1700369_D04.pdf` (PDF, 279 KB, in-module path `doc/`)
>
> Converted from PDF with text extraction; layout, vector diagrams and scanned figures are not preserved. See the source PDF in the repository for the authoritative content.
>
> pages: 1; title: -; author: Trinh, Nam

## Converted content

### Page 1

Readme CBD1700369 D04 
 
 Note / Integration hints 
 
BAC modules 
In our integration we used the latest BMW BAC modules which were available 
(BAC4.3 Version 3.5.0). However, we faced some issues with the BAC modules 
which forced us to modify the code of the BAC modules to be able to do a complete 
flash process successfully. Both issues were submitted to BMW and we suppose they 
get fixed in one of the next BAC4.3 releases. 
We added the modified you your SIP in the folder “IntegrationFiles”: 
 
 
 
The patches are marked in the files with @@@patchedByVector. You can replace the 
original files with these ones as long as these issues exist. 
 
At BMW the issue are registered as BAC-6612 and BAC-6828. 
 
DiagSystemTest 
One testcase (3.1.4) of the DiagSystemTest could not be performed successfully 
since the test suite just stops the CANoe measurement when running this testcase. 
Please contact BMW in case you’re facing the same issue.
