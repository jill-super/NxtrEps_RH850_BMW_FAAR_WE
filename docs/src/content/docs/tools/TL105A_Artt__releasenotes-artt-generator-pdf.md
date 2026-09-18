---
title: 'TL105A_Artt — ReleaseNotes_Artt_Generator'
description: 'Converted PDF document ReleaseNotes_Artt_Generator.pdf from module TL105A_Artt.'
sidebar:
  hidden: true
---

> **Source:** `ReleaseNotes_Artt_Generator.pdf` (PDF, 44 KB, in-module path `doc/`)
>
> Converted from PDF with text extraction; layout, vector diagrams and scanned figures are not preserved. See the source PDF in the repository for the authoritative content.
>
> pages: 14; title: ReleaseNotesReport; author: BMW AG

## Converted content

### Page 1

Page 1 of 14
Copyright (c) 2010 by BMW Group. All rights reserved.
BMW Package Release Notes
Artt_Generator-2.0.2
Package Status:
Released
Author:
BMW Group
Version:
2.0.2
Release Date:
23-Nov-2011

### Page 2

Page 2 of 14
Copyright (c) 2010 by BMW Group. All rights reserved.
1 Revision History
 1.0.1
 03-Oct-2008
Initial revision. CR70051, CR70068.
 1.0.2
 29-Jun-2009
Support of more BAC2.1 templates. CR70168, 
CR70166, CR70167, CR70195, CR70237, 
CR70267.
 1.0.3
 27-Oct-2009
Performance optimization CR70341.
 1.1.0
 11-Nov-2009
User friendliness and portability CR70397, 
CR70343.
 1.1.1
 27-May-2010
CR70519.
 1.2.0
 30-Jun-2010
New validation feature CR70359, CR .
 1.3.0
 11-Oct-2010
AUTOSAR 4.0 schema CR .
 2.0.0
 15-Mar-2011
Behaviour of ValueOf() changed CR71004, 
CR71005.
 2.0.1
 14-Apr-2011
Method ModuleConfAtDefRefTo() added CR71008.
 2.0.2
 23-Nov-2011
CR71146, CR71147.
 Revision
 Date
 Remarks

### Page 3

Page 3 of 14
Copyright (c) 2010 by BMW Group. All rights reserved.
2 Package Enumeration Scheme
3 Package Description
artt is a command line application allowing to generate text files, including source code, from 
AUTOSAR descriptions. As input data artt uses a template file describing static content and 
structure of the desired output and one or more AUTOSAR descriptions, which are serving as 
provider for dynamic content. Since AUTOSAR descriptions are XML files, templates for artt 
typically use XPATH expressions referring to certain elements in the input file.
This package is maintained by BMW AUTOSAR Core Support, via Request Tracker (https://sc-
support.bader-muenchen.de/rt3/) or telephone hotline (+49-89-382-32233).
Every package carries a 3-digit version number. The following table explains how compatibility 
between versions can be determined from the version number:
 Minor Version
 ĺ
A new feature was added. New version is 
backwards compatible to old version.
 Major Version
 ĺ
API of package changed. Versions are not 
compatible. If the new package is used, other 
packages must be changed as well.
 Patch Version
 ĺ
A defect has been fixed. Versions are fully 
compatible.
 Changed Version
 Example
 Compatibility

### Page 4

Page 4 of 14
Copyright (c) 2010 by BMW Group. All rights reserved.
4 Revisions and Modifications
Revision 2.0.2 [Released]
Changed Files:
Compatibility:
Description of Changes:
Item
Description
CR ID:
CR Headline:
Description of Issues:
Changed Files:
Helper.tt
Compatibility:
Fully compatible
Description of Changes:
Changed the implementation to use the correct artt internal 
implicit bool operator to map a ValueNode to a bool.
Marked the helper function BoolValueOf and its wrapper Enabled
() as being obsolete since these helpers can simply be substuitted 
with core artt functions.
Item
Description
CR ID:
71147
CR Headline:
Wrong implementation of BoolValueOf
Description of Issues:
The included template utility file Helper.tt contained a helper 
function BoolValueOf. This implementation was wrong since it did 
not respect the various representations of bool-values allowed by 
the autosar schema.
Changed Files:
artt.chm
Compatibility:
Fully compatible
Item
Description
Description of Changes:
Extended the documentation of ChangeContext method in 
ArGtcBase to reflect that a call to ChangeContext(null) will 
successfully reset the context to the root context AND return false. 
(although one could expect that it returns true because the context 
change was successfull.
CR ID:
71146
CR Headline:
ARTT ChangeContext returns false when called with null as 
parameter.
Description of Issues:
Misleading documentation

### Page 5

Page 5 of 14
Copyright (c) 2010 by BMW Group. All rights reserved.
Revision 2.0.1 [Stable]
artt.chm
Changed Files:
artt.exe
Compatibility:
no restrictions to older AUTOSAR versions
Item
Description
Description of Changes:
Creates XPATH to the <c>MODULE-CONFIGURATION</c> node 
(for AUTOSAR versions before 4.0) 
or the <c>ECUC-MODULE-CONFIGURATION-VALUES</c> 
node (starting with AUTOSAR version 4.0) of the module 
configuration that is based on the module definition with the given 
shortname.
CR ID:
71008
CR Headline:
new method ModuleConfAtDefRefTo()
Description of Issues:
New method ModuleConfAtDefRefTo() added.

### Page 6

Page 6 of 14
Copyright (c) 2010 by BMW Group. All rights reserved.
Revision 2.0.0 [Stable]
Changed Files:
artt.exe
Compatibility:
Instead of writing:
boolean blub = <#= ValueOf(<xpath to BOOLEAN-VALUE>) #>
now it has to be written:
boolean blub = <#= (ValueOf(<xpath to BOOLEAN-VALUE>) == 
true ? “TRUE” : “FALSE”) #>
Item
Description
Description of Changes:
The method ValueOf() now always returns just the string found in 
the template file without an interpretation of it.
CR ID:
71005
CR Headline:
ValueOf-Method shall not try to interprete ECUC-BOOLEAN-
VALUE
Description of Issues:
In versions less the 2 the ValueOf() method returned the string 
found in the tt-file if it was not a boolean value. In case of a 
boolean value, it retruned "TRUE" or "FALSE".
Changed Files:
artt.exe
Compatibility:
no restrictions to older AUTOSAR versions
Item
Description
Description of Changes:
Also in case of a thrown exception in template file an output file is 
generated.
CR ID:
71004
CR Headline:
artt generator shall write output file even in case of error
Description of Issues:
Also for Environment.Exit in template file an outputfile is 
generated.

### Page 7

Page 7 of 14
Copyright (c) 2010 by BMW Group. All rights reserved.
Revision 1.3.0 [Released]
artt.chm
Changed Files:
artt.exe
Compatibility:
no restrictions to older AUTOSAR versions
Item
Description
Description of Changes:
Changed tags of AUTOSAR V4.0 are supported now. Depending 
on the URL given in the template or via the commandline, the tag 
name of AUTOSAR 2.x, 3.x or 4.x is used.
CR ID:
CR Headline:
Handling of the changed tags in AUTOSAR 4.0 schema.
Description of Issues:
- ECUC-MODULE-CONFIGURATION-VALUES instead of 
MODULE-CONFIGURATION (in AR < V3.x)
- ECUC- PARAM-CONF-CONTAINER-DEF instead of PARAM-
CONF-CONTAINER-DEF (in AR < V3.x)

### Page 8

Page 8 of 14
Copyright (c) 2010 by BMW Group. All rights reserved.
Revision 1.2.0 [Stable]
artt.chm
Changed Files:
artt.exe
Compatibility:
Item
Description
Description of Changes:
New set of functions added to manipulate the context using a 
stack: PushContext(), PopContext(), ClearContextStack().
See user guide for more information.
CR ID:
CR Headline:
Push- / PopContext functionality
Description of Issues:
Functionality was needed for Validation of AUTOSAR 
descriptions.
artt.chm
Changed Files:
artt.exe
Compatibility:
Item
Description
Description of Changes:
Implemented validation of AUTOSAR description (EPC) against 
AUTOSAR definition (BMD). Validation can be triggered by 
specifiying the AUTOSAR definition file on the command line. See 
user guide for more information.
CR ID:
70359
CR Headline:
Validation of AUTOSAR descriptions
Description of Issues:
The ARTT generator has no ability to validate the given EPC file 
against the BMD. This has the following disadvantages:
- Existence of nodes can not be ensured
- MIN/MAX/RANGE tags can not be evaluated
- Type checks of variables can not be done
- Uniqueness of container entries can not be verified

*Excerpt: first 8 of 14 pages shown.*
