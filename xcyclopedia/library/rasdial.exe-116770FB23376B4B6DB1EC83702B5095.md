﻿---
title: rasdial.exe | Remote Access Command Line Dial UI
excerpt: What is rasdial.exe?
---

# rasdial.exe 

* File Path: `C:\Windows\SysWOW64\rasdial.exe`
* Description: Remote Access Command Line Dial UI

## Hashes

Type | Hash
-- | --
MD5 | `116770FB23376B4B6DB1EC83702B5095`
SHA1 | `BC48CDF604824AA06DE7D99FEED73520EE17E65A`
SHA256 | `974A95D16A089B476CA8F931CD0D5CD59C8061B04CCE8FFD423AAB555A1DFBE3`
SHA384 | `5FE82B5DB09F54AC739D86478AA4340CD6BB93B8638D0B52CD160A81F908D0FA7E2BE72CE48EA032CCC4DB6571A8DDF6`
SHA512 | `929C1C030DC8B1D47606F88F586E59929B6D126BE0190870885250034BF6F06E1D9EF29C29730AF02E80A0D64E4D23663C3EA5EE248646B414EBD1494DE59A64`
SSDEEP | `384:hzej6G9rUtmjYGFqR0XONQQ0Tf6WQVWTgK:drcq5QQAfccg`
IMP | `5C49C69DC9F9E8B85CB908313C7FCFF4`
PESHA1 | `90E0D3A90870008D8468C2D225C4C2B2049D7775`
PE256 | `CB2B2B750AF5A4D20CABF7F10759A087216C840B81494D04013D19542F0FC941`

## Runtime Data

### Usage (stdout):
```cmhg
USAGE:
	C:\Windows\SysWOW64\rasdial.exe entryname [username [password|*]] [/DOMAIN:domain]
		[/PHONE:phonenumber] [/CALLBACK:callbacknumber]
		[/PHONEBOOK:phonebookfile] [/PREFIXSUFFIX]

	C:\Windows\SysWOW64\rasdial.exe [entryname] /DISCONNECT

	C:\Windows\SysWOW64\rasdial.exe

	Please refer to our privacy statement at 
	'https://go.microsoft.com/fwlink/?LinkId=521839'


```

### Loaded Modules:

Path |
-- |
C:\Windows\SYSTEM32\ntdll.dll |
C:\Windows\System32\wow64.dll |
C:\Windows\System32\wow64cpu.dll |
C:\Windows\System32\wow64win.dll |
C:\Windows\SysWOW64\rasdial.exe |


## Signature

* Status: Signature verified.
* Serial: `3300000266BD1580EFA75CD6D3000000000266`
* Thumbprint: `A4341B9FD50FB9964283220A36A1EF6F6FAA7840`
* Issuer: CN=Microsoft Windows Production PCA 2011, O=Microsoft Corporation, L=Redmond, S=Washington, C=US
* Subject: CN=Microsoft Windows, O=Microsoft Corporation, L=Redmond, S=Washington, C=US

## File Metadata

* Original Filename: RASDIAL.EXE.MUI
* Product Name: Microsoft Windows Operating System
* Company Name: Microsoft Corporation
* File Version: 10.0.17763.1 (WinBuild.160101.0800)
* Product Version: 10.0.17763.1
* Language: English (United States)
* Legal Copyright:  Microsoft Corporation. All rights reserved.
* Machine Type: 32-bit

## File Scan

* VirusTotal Detections: 0/70
* VirusTotal Link: https://www.virustotal.com/gui/file/974a95d16a089b476ca8f931cd0d5cd59c8061b04cce8ffd423aab555a1dfbe3/detection/


## Possible Misuse

*The following table contains possible examples of `rasdial.exe` being misused. While `rasdial.exe` is **not** inherently malicious, its legitimate functionality can be abused for malicious purposes.*

Source | Source File | Example | License
-- | -- | -- | --
[sigma](https://github.com/Neo23x0/sigma) | [win_susp_rasdial_activity.yml](https://github.com/Neo23x0/sigma/blob/master/rules/windows/process_creation/win_susp_rasdial_activity.yml) | `title: Suspicious RASdial Activity` | [DRL 1.0](https://github.com/Neo23x0/sigma/blob/master/LICENSE.Detection.Rules.md)
[sigma](https://github.com/Neo23x0/sigma) | [win_susp_rasdial_activity.yml](https://github.com/Neo23x0/sigma/blob/master/rules/windows/process_creation/win_susp_rasdial_activity.yml) | `description: Detects suspicious process related to rasdial.exe` | [DRL 1.0](https://github.com/Neo23x0/sigma/blob/master/LICENSE.Detection.Rules.md)
[sigma](https://github.com/Neo23x0/sigma) | [win_susp_rasdial_activity.yml](https://github.com/Neo23x0/sigma/blob/master/rules/windows/process_creation/win_susp_rasdial_activity.yml) | `- rasdial.exe` | [DRL 1.0](https://github.com/Neo23x0/sigma/blob/master/LICENSE.Detection.Rules.md)



MIT License. Copyright (c) 2020 Strontic.


