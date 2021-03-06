﻿---
title: ktmutil.exe | Kernel Transaction Management Utility
excerpt: What is ktmutil.exe?
---

# ktmutil.exe 

* File Path: `C:\WINDOWS\system32\ktmutil.exe`
* Description: Kernel Transaction Management Utility

## Hashes

Type | Hash
-- | --
MD5 | `A77A5364E36FCB1573C4D41AEB8BDCCD`
SHA1 | `FAE711626E985D133CBE0A3F942FD4FEDED76BB4`
SHA256 | `1AFBBE861F01F4D29707EA260AABD546CB25FEF939EF615F5354B3383DEE1038`
SHA384 | `636A9CF916C69B0CADB7A826BCC323AB3328C223D4CA8869507F86D12D8798FD9E8E4E882711B5DFDCF2D673D85D4137`
SHA512 | `BE5406CAE81F171344B1E4D97CCDF34D112356C5DC22F07C872476CD017176AED522D38F4A2ADB1BDC768BDC307596A47D0B0426C40A1C4527578AE42A875F20`
SSDEEP | `384:hR8zefNzVpqIuU+N22F0FmNOf2TCS3M3/uW+jW:YeFVnFwN/jM3/u`

## Runtime Data

### Usage (stdout):
```cmhg
The KTMUTIL utility requires that you have administrative privileges.

```

## Signature

* Status: Signature verified.
* Serial: `330000023241FB59996DCC4DFF000000000232`
* Thumbprint: `FF82BC38E1DA5E596DF374C53E3617F7EDA36B06`
* Issuer: CN=Microsoft Windows Production PCA 2011, O=Microsoft Corporation, L=Redmond, S=Washington, C=US
* Subject: CN=Microsoft Windows, O=Microsoft Corporation, L=Redmond, S=Washington, C=US

## File Metadata

* Original Filename: ktmutil.exe.mui
* Product Name: Microsoft Windows Operating System
* Company Name: Microsoft Corporation
* File Version: 10.0.18362.1 (WinBuild.160101.0800)
* Product Version: 10.0.18362.1
* Language: English (United States)
* Legal Copyright:  Microsoft Corporation. All rights reserved.


## File Similarity (ssdeep match)

File | Score
-- | --
[C:\Windows\system32\ktmutil.exe](ktmutil.exe-4EA868EA2484EB3DE0598855BA3D8926.md) | 63


## Additional Info*

**The information below is copied from [MicrosoftDocs](https://github.com/MicrosoftDocs/windowsserverdocs), which is maintained by [Microsoft](https://opensource.microsoft.com/codeofconduct/). Available under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/) license.*

---

## ktmutil

Starts the Kernel Transaction Manager utility. If used without parameters, **ktmutil** displays available subcommands.

### Syntax

```
ktmutil list tms
ktmutil list transactions [{TmGUID}]
ktmutil resolve complete {TmGUID} {RmGUID} {EnGUID}
ktmutil resolve commit {TxGUID}
ktmutil resolve rollback {TxGUID}
ktmutil force commit {GUID}
ktmutil force rollback {GUID}
ktmutil forget
```

### Examples


To force an Indoubt transaction with GUID 311a9209-03f4-11dc-918f-00188b8f707b to commit, type:

```
ktmutil force commit {311a9209-03f4-11dc-918f-00188b8f707b}
```

### Additional References

- [Command-Line Syntax Key](https://github.com/MicrosoftDocs/windowsserverdocs/tree/master/WindowsServerDocs/administration/windows-commands/command-line-syntax-key.md)

---



MIT License. Copyright (c) 2020 Strontic.


