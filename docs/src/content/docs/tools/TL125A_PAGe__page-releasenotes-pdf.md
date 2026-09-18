---
title: 'TL125A_PAGe — PAGe_ReleaseNotes'
description: 'Converted PDF document PAGe_ReleaseNotes.pdf from module TL125A_PAGe.'
sidebar:
  hidden: true
---

> **Source:** `PAGe_ReleaseNotes.pdf` (PDF, 117 KB, in-module path `doc/`)
>
> Converted from PDF with text extraction; layout, vector diagrams and scanned figures are not preserved. See the source PDF in the repository for the authoritative content.
>
> pages: 3; title: -; author: -

## Converted content

### Page 1

Release Notes PAGe
Project adaptive BMW AUTOSAR Core Rel. 1
Author BMW AG
Release Date 2017-11-09
Version 1.1.0
Status Release
Hotline +49 89 382 - 22522
Contact abac@bmw.de
https://asc.bmw.com/jira/browse/BSUP (extern)
https://asc.bmwgroup.net/jira/browse/BSUP (intern)
Company
Bayerische
Motoren Werke
Aktiengesellschaft
Postal address
BMW AG
80788 München
Office address
Forschungs- und
Innovationszentrum
(FIZ)
Hufelandstr. 1
80937 München
Telephone
Switchboard
+49 89 382-0
Internet
www.bmwgroup.com
Revision History
Version Date Issues
1.1.0 2017-11-09 BAC-6409, BAC-6509, BAC-6150
1.0.0 2017-06-29
ReleaseNotes_PAGe, Version 1.1.0, Software Platforms Page 1 of 3

### Page 2

1 Module Description
Tool to generate text from AUTOSAR paramconf.
2 Revisions and Modiﬁcations
Revision 1.1.0 [Released]
Item Description
CR ID: BAC-6409
CR Headline: PAGe should only rely on Python std library modules.
Description of Issues: The dependecy of lxml shall be removed
Description of Changes: The parsing of the XML was changed so PAGe now builds an
internal model and does not rely on xpath expressions.
Changed Files: utility/utility.py
utility/exceptions.py
core/command.py
codeparts/codepart.py
utility/xpath_resolver.py
core/model.py
core/xmlcache.py
core/verify.py
Compatibility:
Item Description
CR ID: BAC-6509
CR Headline: PAGe must be more robust for shortnames
Description of Issues: Improve Robustness of Shortnamepath operations
Description of Changes: Allow strings and trailing slashes in shortnamepaths.
Changed Files: codeparts/inputtext.py
utility/utility.py
codeparts/inputpart.py
core/model.py
Compatibility:
Item Description
CR ID: BAC-6150
CR Headline: BAC 4.3: Provide shell wrapper/.cmd-file for PAGe
Description of Issues: Add a shell script to wrap page call
Description of Changes: A shell script is provided in the bin directory. This allows calling
page without manually setting the PYTHONPATH.
Changed Files: bin/page
Compatibility:
ReleaseNotes_PAGe, Version 1.1.0, Software Platforms Page 2 of 3

### Page 3

Revision 1.0.0 [Released]
Item Description
CR ID:
CR Headline: Initial Release for SP2021
Description of Issues: Initial Release for SP2021
Description of Changes: Initial Release for SP2021
Changed Files:
Compatibility:
ReleaseNotes_PAGe, Version 1.1.0, Software Platforms Page 3 of 3
