﻿---
title: powercfg.exe | Power Settings Command-Line Tool
excerpt: What is powercfg.exe?
---

# powercfg.exe 

* File Path: `C:\Windows\SysWOW64\powercfg.exe`
* Description: Power Settings Command-Line Tool

## Hashes

Type | Hash
-- | --
MD5 | `9D71DBDD3AD017EC69554ACF9CAADD05`
SHA1 | `0989525DDA5F937A4895F2A53A4319FF16890B03`
SHA256 | `7B48D1D9EB8ECC4E59F76CABAC1A9E009E5A39F0524FA8EEA29A3ACBC8CD32C1`
SHA384 | `F103D13F06DE46E4E5CF64484E16D97EFD609E1F0230C889AA75FDC5F821AF2D8CE9F1123EECFA907DE4A16DF7D2FA06`
SHA512 | `D145D011D8E344A650D4E60579BD0CE5D8BD33645342CA20F44D62013B6BDC4935F4E2E272D80410E17B3D2464D3C9B1E8FDA2A3657E0606F301CF24B945B1B3`
SSDEEP | `1536:shBwU9X3QNgjjy8uAQBc2vkgNszy+yfPildu/iaxczLMYe4/z0ls:wwUp3zOvAK5Ky9iQiaxULMYeCC`
IMP | `A4CAEF3F5A6B4DE55898C86E84355E40`
PESHA1 | `D158196F06A6F9B9E4BDE3A544396E4792ED9F2A`
PE256 | `6888BA6E89D221CABD306F93AAE8725E879B6183F07ABA4B21319378175ED913`

## Runtime Data

### Usage (stdout):
```cmhg

POWERCFG /COMMAND [ARGUMENTS]

Description:
  Enables users to control power settings on a local system.

  For detailed command and option information, run "POWERCFG /? <COMMAND>"

Command List:
  /LIST, /L          Lists all power schemes.

  /QUERY, /Q         Displays the contents of a power scheme.

  /CHANGE, /X        Modifies a setting value in the current power scheme.

  /CHANGENAME        Modifies the name and description of a power scheme.

  /DUPLICATESCHEME   Duplicates a power scheme.

  /DELETE, /D        Deletes a power scheme.

  /DELETESETTING     Deletes a power setting.

  /SETACTIVE, /S     Makes a power scheme active on the system.

  /GETACTIVESCHEME   Retrieves the currently active power scheme.

  /SETACVALUEINDEX   Sets the value associated with a power setting
                     while the system is powered by AC power.

  /SETDCVALUEINDEX   Sets the value associated with a power setting
                     while the system is powered by DC power.

  /IMPORT            Imports all power settings from a file.

  /EXPORT            Exports a power scheme to a file.

  /ALIASES           Displays all aliases and their corresponding GUIDs.

  /GETSECURITYDESCRIPTOR
                     Gets a security descriptor associated with a specified
                     power setting, power scheme, or action.

  /SETSECURITYDESCRIPTOR
                     Sets a security descriptor associated with a
                     power setting, power scheme, or action.

  /HIBERNATE, /H     Enables and disables the hibernate feature.

  /AVAILABLESLEEPSTATES, /A
                     Reports the sleep states available on the system.

  /DEVICEQUERY       Returns a list of devices that meet specified criteria.

  /DEVICEENABLEWAKE  Enables a device to wake the system from a sleep state.

  /DEVICEDISABLEWAKE Disables a device from waking the system from a sleep
                     state.

  /LASTWAKE          Reports information about what woke the system from the
                     last sleep transition.

  /WAKETIMERS        Enumerates active wake timers.

  /REQUESTS          Enumerates application and driver Power Requests.

  /REQUESTSOVERRIDE  Sets a Power Request override for a particular Process,
                     Service, or Driver.

  /SYSTEMSLEEPDIAGNOSTICS
                     Generates a diagnostic report of system sleep transitions.

  /SYSTEMPOWERREPORT Generates a diagnostic system power transition report.

  /POWERTHROTTLING   Control power throttling for an application.



```

### Usage (stderr):
```cmhg
Invalid Parameters -- try "/?" for help

```

### Loaded Modules:

Path |
-- |
C:\Windows\SYSTEM32\ntdll.dll |
C:\Windows\System32\wow64.dll |
C:\Windows\System32\wow64cpu.dll |
C:\Windows\System32\wow64win.dll |
C:\Windows\SysWOW64\powercfg.exe |


## Signature

* Status: Signature verified.
* Serial: `3300000266BD1580EFA75CD6D3000000000266`
* Thumbprint: `A4341B9FD50FB9964283220A36A1EF6F6FAA7840`
* Issuer: CN=Microsoft Windows Production PCA 2011, O=Microsoft Corporation, L=Redmond, S=Washington, C=US
* Subject: CN=Microsoft Windows, O=Microsoft Corporation, L=Redmond, S=Washington, C=US

## File Metadata

* Original Filename: PowerCfg.exe
* Product Name: Microsoft Windows Operating System
* Company Name: Microsoft Corporation
* File Version: 10.0.19041.1 (WinBuild.160101.0800)
* Product Version: 10.0.19041.1
* Language: English (United States)
* Legal Copyright:  Microsoft Corporation. All rights reserved.
* Machine Type: 32-bit

## File Scan

* VirusTotal Detections: 0/75
* VirusTotal Link: https://www.virustotal.com/gui/file/7b48d1d9eb8ecc4e59f76cabac1a9e009e5a39f0524fa8eea29a3acbc8cd32c1/detection





MIT License. Copyright (c) 2020 Strontic.


