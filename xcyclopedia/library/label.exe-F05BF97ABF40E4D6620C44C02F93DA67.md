﻿---
title: label.exe | Disk Label Utility
excerpt: What is label.exe?
---

# label.exe 

* File Path: `C:\Windows\SysWOW64\label.exe`
* Description: Disk Label Utility

## Hashes

Type | Hash
-- | --
MD5 | `F05BF97ABF40E4D6620C44C02F93DA67`
SHA1 | `2BAE11E3A9B67B3692D55D4481BB2640101537A5`
SHA256 | `332FA83BDC982AB5A509EFF6FDAC3161034BF55B32B7F7DC3C7551FE3A6A0CBC`
SHA384 | `5C029D1925A7645E96F86576D219DFD7FE0FBA0D7D951E3F0915621F7E25A761B2FFC8EC3AA6C6BB50BFB436877E786F`
SHA512 | `5CE47F545883B4BAE5DC2E3090B39753A21862AB3C505B1CA8F42BB04F7686DAB790939FC528C2ECA37B46AE6393E74DD85B40037F02390FF30A7A19049EFD67`
SSDEEP | `192:ukoZDUEfi8wI0THvYBB+vhCl4EIC2SDp9td5kdtm1kgWStjWxoNNezd1O:WZgrIVUhCl2C2gPANgWStjWxoOzd`
IMP | `89817B62874F5050E534349B8EB33EB0`
PESHA1 | `8B4E62A8DC3F7A09F21F7EB0C1D26DC3A1E071AE`
PE256 | `47AB7C7912248BD69277A1A9ECE1BAE2CC4D6C9B45FA0ADE088AD53B4E4BB72D`

## Runtime Data

### Usage (stdout):
```cmhg
Creates, changes, or deletes the volume label of a disk.

LABEL [drive:][label]
LABEL [/MP] [volume] [label]

  drive:          Specifies the drive letter of a drive.
  label           Specifies the label of the volume.
  /MP             Specifies that the volume should be treated as a
                  mount point or volume name.
  volume          Specifies the drive letter (followed by a colon),
                  mount point, or volume name.  If volume name is specified,
                  the /MP flag is unnecessary.

```

### Loaded Modules:

Path |
-- |
C:\Windows\SYSTEM32\ntdll.dll |
C:\Windows\System32\wow64.dll |
C:\Windows\System32\wow64cpu.dll |
C:\Windows\System32\wow64win.dll |
C:\Windows\SysWOW64\label.exe |


## Signature

* Status: Signature verified.
* Serial: `33000001C422B2F79B793DACB20000000001C4`
* Thumbprint: `AE9C1AE54763822EEC42474983D8B635116C8452`
* Issuer: CN=Microsoft Windows Production PCA 2011, O=Microsoft Corporation, L=Redmond, S=Washington, C=US
* Subject: CN=Microsoft Windows, O=Microsoft Corporation, L=Redmond, S=Washington, C=US

## File Metadata

* Original Filename: Label.Exe
* Product Name: Microsoft Windows Operating System
* Company Name: Microsoft Corporation
* File Version: 10.0.17763.1 (WinBuild.160101.0800)
* Product Version: 10.0.17763.1
* Language: English (United States)
* Legal Copyright:  Microsoft Corporation. All rights reserved.
* Machine Type: 32-bit

## File Scan

* VirusTotal Detections: 0/68
* VirusTotal Link: https://www.virustotal.com/gui/file/332fa83bdc982ab5a509eff6fdac3161034bf55b32b7f7dc3c7551fe3a6a0cbc/detection/


## Possible Misuse

*The following table contains possible examples of `label.exe` being misused. While `label.exe` is **not** inherently malicious, its legitimate functionality can be abused for malicious purposes.*

Source | Source File | Example | License
-- | -- | -- | --
[signature-base](https://github.com/Neo23x0/signature-base) | [apt_apt29_grizzly_steppe.yar](https://github.com/Neo23x0/signature-base/blob/master/yara/apt_apt29_grizzly_steppe.yar) | $ = "\x0D\x0AVolume label: " | [CC BY-NC 4.0](https://github.com/Neo23x0/signature-base/blob/master/LICENSE)
[signature-base](https://github.com/Neo23x0/signature-base) | [gen_Excel4Macro_Sharpshooter.yar](https://github.com/Neo23x0/signature-base/blob/master/yara/gen_Excel4Macro_Sharpshooter.yar) | // ' 0018     23 LABEL : Cell Value, String Constant - build-in-name 1 Auto_Open | [CC BY-NC 4.0](https://github.com/Neo23x0/signature-base/blob/master/LICENSE)
[signature-base](https://github.com/Neo23x0/signature-base) | [gen_win_privesc.yar](https://github.com/Neo23x0/signature-base/blob/master/yara/gen_win_privesc.yar) | $s1 = "<Label x:Name=\"lblPort\" Content=\"Port:\"  HorizontalAlignment=\"Left\" Height=\"28\" Margin=\"10,0,0,0\" Width=\"35\"/>" fullword ascii | [CC BY-NC 4.0](https://github.com/Neo23x0/signature-base/blob/master/LICENSE)

## Additional Info*

**The information below is copied from [MicrosoftDocs](https://github.com/MicrosoftDocs/windowsserverdocs), which is maintained by [Microsoft](https://opensource.microsoft.com/codeofconduct/). Available under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/) license.*

---

## label

Creates, changes, or deletes the volume label (that is, the name) of a disk. If used without parameters, the **label** command changes the current volume label or deletes the existing label.

### Syntax

```
label [/mp] [<volume>] [<label>]
```

#### Parameters

| Parameter | Description |
| --------- | ----------- |
| /mp | Specifies that the volume should be treated as a mount point or volume name. |
| `<volume>` | Specifies a drive letter (followed by a colon), mount point, or volume name. If a volume name is specified, the **/mp** parameter is unnecessary. |
| `<label>` | Specifies the label for the volume. |
| /? | Displays help at the command prompt. |

### Remarks

- Windows displays the volume label and serial number (if it has one) as part of the directory listing.

- An NTFS volume label can be up to 32 characters in length, including spaces. NTFS volume labels retain and display the case that was used when the label was created.

### Examples

To label a disk in drive A that contains sales information for July, type:

```
label a:sales-july
```

To view and delete the current label for drive C, follow these steps:

1. At the command prompt, type:

   ```
   label
   ```

   Output similar to the following should be displayed:

   ```
   Volume in drive C: is Main Disk
   Volume Serial Number is 6789-ABCD
   Volume label (32 characters, ENTER for none)?
   ```

2. Press ENTER. The following prompt should be displayed:

   ```
   Delete current volume label (Y/N)?
   ```

3. Press **Y** to delete the current label, or **N** if you want to keep the existing label.

### Additional References

- [Command-Line Syntax Key](https://github.com/MicrosoftDocs/windowsserverdocs/tree/master/WindowsServerDocs/administration/windows-commands/command-line-syntax-key.md)

---



MIT License. Copyright (c) 2020 Strontic.


