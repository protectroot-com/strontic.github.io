﻿---
title: mountvol.exe | Mount Volume Utility
excerpt: What is mountvol.exe?
---

# mountvol.exe 

* File Path: `C:\Windows\SysWOW64\mountvol.exe`
* Description: Mount Volume Utility

## Hashes

Type | Hash
-- | --
MD5 | `15AA34D64152527D4542546C3CFAC9A9`
SHA1 | `4C7A7DE6005873D751C942671EAF7B4B50635452`
SHA256 | `3408B443926447C03A7575C563163B8E9ADF54AAE9F4FAD959A4A61D588FA234`
SHA384 | `079A6267617262F1C837C9DAB84D2A291B2E6DC379172D2B35FCB1DA958396256EEAE58ED8711EB9FE1FA5B1F29FBCED`
SHA512 | `926341DEC7FBF72519B58E92A76BAA125D1AEC9EE58BE294E0D2014BAD8334C3AD9B91940D804121C6F3FCAD22B144E46B376D5655A258E75059B9B529B6BBD6`
SSDEEP | `192:/lI1xnAe4RQEXUbgOW0xDAGpfO2cjt9aO0uUOxPtLHwI7ER2NuzkkWQFWfK+:/sGUEOWgAG1OtGO0YxVLQIXNuIkWQFW`
IMP | `30F2C65A9103A7536B77118A741917B8`
PESHA1 | `89037692831A333ECFE83B1AFC3D87E5AE107B20`
PE256 | `6162604C611198C68377DD4FB97E71ED68B5F59BCD9A32AD51A5A59AD27FE1C8`

## Runtime Data

### Usage (stdout):
```cmhg
Creates, deletes, or lists a volume mount point.

MOUNTVOL [drive:]path VolumeName
MOUNTVOL [drive:]path /D
MOUNTVOL [drive:]path /L
MOUNTVOL [drive:]path /P
MOUNTVOL /R
MOUNTVOL /N
MOUNTVOL /E

    path        Specifies the existing NTFS directory where the mount
                point will reside.
    VolumeName  Specifies the volume name that is the target of the mount
                point.
    /D          Removes the volume mount point from the specified directory.
    /L          Lists the mounted volume name for the specified directory.
    /P          Removes the volume mount point from the specified directory,
                dismounts the volume, and makes the volume not mountable.
                You can make the volume mountable again by creating a volume
                mount point.
    /R          Removes volume mount point directories and registry settings
                for volumes that are no longer in the system.
    /N          Disables automatic mounting of new volumes.
    /E          Re-enables automatic mounting of new volumes.

Possible values for VolumeName along with current mount points are:

    \\?\Volume{7c775138-0000-0000-0000-100000000000}\
        C:\


```

### Loaded Modules:

Path |
-- |
C:\Windows\SYSTEM32\ntdll.dll |
C:\Windows\System32\wow64.dll |
C:\Windows\System32\wow64cpu.dll |
C:\Windows\System32\wow64win.dll |
C:\Windows\SysWOW64\mountvol.exe |


## Signature

* Status: Signature verified.
* Serial: `33000001C422B2F79B793DACB20000000001C4`
* Thumbprint: `AE9C1AE54763822EEC42474983D8B635116C8452`
* Issuer: CN=Microsoft Windows Production PCA 2011, O=Microsoft Corporation, L=Redmond, S=Washington, C=US
* Subject: CN=Microsoft Windows, O=Microsoft Corporation, L=Redmond, S=Washington, C=US

## File Metadata

* Original Filename: MOUNTVOL.EXE
* Product Name: Microsoft Windows Operating System
* Company Name: Microsoft Corporation
* File Version: 10.0.17763.1 (WinBuild.160101.0800)
* Product Version: 10.0.17763.1
* Language: English (United States)
* Legal Copyright:  Microsoft Corporation. All rights reserved.
* Machine Type: 32-bit

## File Scan

* VirusTotal Detections: 0/72
* VirusTotal Link: https://www.virustotal.com/gui/file/3408b443926447c03a7575c563163b8e9adf54aae9f4fad959a4a61d588fa234/detection/

## File Similarity (ssdeep match)

File | Score
-- | --
[C:\WINDOWS\SysWOW64\mountvol.exe](mountvol.exe-0B61BCAED563051163D83B4F835F7AAA.md) | 44


## Additional Info*

**The information below is copied from [MicrosoftDocs](https://github.com/MicrosoftDocs/windowsserverdocs), which is maintained by [Microsoft](https://opensource.microsoft.com/codeofconduct/). Available under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/) license.*

---

## mountvol

Creates, deletes, or lists a volume mount point. You can also link volumes without requiring a drive letter.

### Syntax

```
mountvol [<drive>:]<path volumename>
mountvol [<drive>:]<path> /d
mountvol [<drive>:]<path> /l
mountvol [<drive>:]<path> /p
mountvol /r
mountvol [/n|/e]
mountvol <drive>: /s
```

#### Parameters

| Parameter | Description |
| --------- | ----------- |
| `[<drive>:]<path>` | Specifies the existing NTFS directory where the mount point will reside. |
| `<volumename>` | Specifies the volume name that is the target of the mount point. The volume name uses the following syntax, where *GUID* is a globally unique identifier: `\\?\volume\{GUID}\`. The brackets `{ }` are required. |
| /d | Removes the volume mount point from the specified folder. |
| /l | Lists the mounted volume name for the specified folder. |
| /p | Removes the volume mount point from the specified directory, dismounts the basic volume, and takes the basic volume offline, making it unmountable. If other processes are using the volume, **mountvol** closes any open handles before dismounting the volume. |
| /r | Removes volume mount point directories and registry settings for volumes that are no longer in the system, preventing them from being automatically mounted and given their former volume mount point(s) when added back to the system. |
| /n | Disables automatic mounting of new basic volumes. New volumes are not mounted automatically when added to the system. |
| /e | Re-enables automatic mounting of new basic volumes. |
| /s | Mounts the EFI system partition on the specified drive. |
| /? | Displays help at the command prompt. |

### Remarks

- If you dismount your volume while using the **/p** parameter, the volume list will show the volume as not mounted until a volume mount point is created.

- If your volume has more than one mount point, use **/d** to remove the additional mount points before using **/p**. You can make the basic volume mountable again by assigning a volume mount point.

- If you need to expand your volume space without reformatting or replacing a hard drive, you can add a mount path to another volume. The benefit of using one volume with several mount paths is that you can access all local volumes by using a single drive letter (such as `C:`). You don't need to remember which volume corresponds to which drive letterâ€”although you can still mount local volumes and assign them drive letters.

### Examples

To create a mount point, type:

```
mountvol \sysmount \\?\volume\{2eca078d-5cbc-43d3-aff8-7e8511f60d0e}\
```

### Additional References

- [Command-Line Syntax Key](https://github.com/MicrosoftDocs/windowsserverdocs/tree/master/WindowsServerDocs/administration/windows-commands/command-line-syntax-key.md)

---



MIT License. Copyright (c) 2020 Strontic.


