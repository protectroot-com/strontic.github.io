﻿---
title: ReAgentc.exe | Microsoft Windows Recovery Agent
excerpt: What is ReAgentc.exe?
---

# ReAgentc.exe 

* File Path: `C:\Windows\system32\ReAgentc.exe`
* Description: Microsoft Windows Recovery Agent

## Hashes

Type | Hash
-- | --
MD5 | `4FF3D4C021431F4A09A363E6F1D5B550`
SHA1 | `DD63841FA98500C0FCB54991201696D7F3B26607`
SHA256 | `93CD96077494331129E20718A8E9B21E7BAD04DA6CE563FCC56D03AE986DC800`
SHA384 | `8FADA4FB844BD67154EB96B58CB642EF8B8B4E835B1D7DAC78E1F4181913D84044AE64FA8DEFEE7BA999ACEC6AD7AC8D`
SHA512 | `FD5A0281392AC56F67E555D14177DE65BA293B69CD0A2315065BA938196AC71073D407A2C1BF40FFECD5AAF1D4E592B5C2585A1751889D312E4E1264127014A1`
SSDEEP | `768:K+xfqLK+0Snlpr/yLg2oobvPk/l6s9owLptiAJ:KuhgtA9oow/l62owPiAJ`
IMP | `2455C15D4650B236D7331E66AA15D2CD`
PESHA1 | `041378BFD205ED4413A85ECD1DD4797FC88E8EF7`
PE256 | `51703251823B212DD86B746323E9C40FFB09F9F54B113EAF285F88C2A635B68A`

## Runtime Data

### Usage (stdout):
```cmhg

Configures the Windows Recovery Environment (Windows RE) and system reset.

REAGENTC.EXE <command> <arguments>

The following commands can be specified:

  /info             - Displays Windows RE and system reset configuration
                      information.
  /setreimage       - Sets the location of the custom Windows RE image.
  /enable           - Enables Windows RE.
  /disable          - Disables Windows RE.
  /boottore         - Configures the system to start Windows RE next time the
                      system starts up.
  /setbootshelllink - Adds an entry to the Reset and Restore page in the boot
                      menu.

For more information about these commands and their arguments, type
REAGENTC.EXE <command> /?.

  Examples:
    REAGENTC.EXE /setreimage /?
    REAGENTC.EXE /disable /?


```

### Usage (stderr):
```cmhg

Configures the Windows Recovery Environment (Windows RE) and system reset.

REAGENTC.EXE <command> <arguments>

The following commands can be specified:

  /info             - Displays Windows RE and system reset configuration
                      information.
  /setreimage       - Sets the location of the custom Windows RE image.
  /enable           - Enables Windows RE.
  /disable          - Disables Windows RE.
  /boottore         - Configures the system to start Windows RE next time the
                      system starts up.
  /setbootshelllink - Adds an entry to the Reset and Restore page in the boot
                      menu.

For more information about these commands and their arguments, type
REAGENTC.EXE <command> /?.

  Examples:
    REAGENTC.EXE /setreimage /?
    REAGENTC.EXE /disable /?


```

### Loaded Modules:

Path |
-- |
C:\Windows\System32\ADVAPI32.dll |
C:\Windows\System32\GDI32.dll |
C:\Windows\System32\gdi32full.dll |
C:\Windows\System32\KERNEL32.DLL |
C:\Windows\System32\KERNELBASE.dll |
C:\Windows\System32\msvcp_win.dll |
C:\Windows\System32\msvcrt.dll |
C:\Windows\SYSTEM32\ntdll.dll |
C:\Windows\system32\ReAgentc.exe |
C:\Windows\System32\RPCRT4.dll |
C:\Windows\System32\sechost.dll |
C:\Windows\System32\ucrtbase.dll |
C:\Windows\System32\USER32.dll |
C:\Windows\System32\win32u.dll |


## Signature

* Status: Signature verified.
* Serial: `33000001C422B2F79B793DACB20000000001C4`
* Thumbprint: `AE9C1AE54763822EEC42474983D8B635116C8452`
* Issuer: CN=Microsoft Windows Production PCA 2011, O=Microsoft Corporation, L=Redmond, S=Washington, C=US
* Subject: CN=Microsoft Windows, O=Microsoft Corporation, L=Redmond, S=Washington, C=US

## File Metadata

* Original Filename: reagentc.exe.mui
* Product Name: Microsoft Windows Operating System
* Company Name: Microsoft Corporation
* File Version: 10.0.17763.1 (WinBuild.160101.0800)
* Product Version: 10.0.17763.1
* Language: English (United States)
* Legal Copyright:  Microsoft Corporation. All rights reserved.
* Machine Type: 64-bit

## File Scan

* VirusTotal Detections: 0/71
* VirusTotal Link: https://www.virustotal.com/gui/file/93cd96077494331129e20718a8e9b21e7bad04da6ce563fcc56d03ae986dc800/detection/





MIT License. Copyright (c) 2020 Strontic.


