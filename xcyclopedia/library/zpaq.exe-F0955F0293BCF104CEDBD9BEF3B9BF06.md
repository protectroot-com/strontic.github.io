﻿---
title: zpaq.exe | 
excerpt: What is zpaq.exe?
---

# zpaq.exe 

* File Path: `C:\Program Files\PeaZip\res\zpaq\zpaq.exe`

## Hashes

Type | Hash
-- | --
MD5 | `F0955F0293BCF104CEDBD9BEF3B9BF06`
SHA1 | `9234781EC8FD66172AFA50FFA37A3D0F9C1D3037`
SHA256 | `7A94B4F1D6323A758C7B0B6344036F166BFF0FD44F1C3C86F05B3688023496CB`
SHA384 | `8D1E24DA276EB5F9DD86DC875CFE9ED92D5155DD57F199ED35B212F36181CFD37983AF93E4F283D6E4A0FA326EA1581D`
SHA512 | `A4D53801689BF4F362CA86142B9BB2C2165E4E2B61937A4352963A1A78D8C7357DA77EBE917C869CA8446E980FCDF0ABB968253E8CE9218550BA447AD3A1101D`
SSDEEP | `24576:kLtrZo0gn7HFHqdBzAD+qzBbWLG1F1S9eUaU000K0000d000R000:khrZjgnLFKdBzK9zBbWlB`
IMP | `AC3973BCC0C9F23105BBD985DE43A5E9`
PESHA1 | `EA132100D5161703DBB10D8F4A402D5D6AF71CBB`
PE256 | `E9C7608681F8C647D3EBF1964A931E1B7BB106E09822F1A4EFD0364FB915F9E6`

## Runtime Data

### Usage (stdout):
```cmhg
zpaq v7.15 journaling archiver, compiled Aug 17 2016
Unknown option ignored: --help
Usage: zpaq command archive[.zpaq] files... -options...
Files... may be directory trees. Default is the whole archive.
Use * or ???? in archive name for multi-part or "" for empty.
Commands:
   a  add         Append files to archive if dates have changed.
   x  extract     Extract most recent versions of files.
   l  list        List or compare external files to archive by dates.
Options:
  -all [N]        Extract/list versions in N [4] digit directories.
  -f -force       Add: append files if contents have changed.
                  Extract: overwrite existing output files.
                  List: compare file contents instead of dates.
  -index F        Extract: create index F for archive.
                  Add: create suffix for archive indexed by F, update F.
  -key X          Create or access encrypted archive with password X.
  -mN  -method N  Compress level N (0..5 = faster..better, default 1).
  -noattributes   Ignore/don't save file attributes or permissions.
  -not files...   Exclude. * and ? match any string or char.
       =[+-#^?]   List: exclude by comparison result.
  -only files...  Include only matches (default: *).
  -repack F [X]   Extract to new archive F with key X (default: none).
  -sN -summary N  List: show top N sorted by size. -1: show frag IDs.
                  Add/Extract: if N > 0 show brief progress.
  -test           Extract: verify but do not write files.
  -tN -threads N  Use N threads (default: 0 = 0 cores).
  -to out...      Rename files... to out... or all to out/all.
  -until N        Roll back archive to N'th update or -N from end.
  -until 2020-09-24 22:19:47  Set date, roll back (UT, default time: 235959).

```

### Loaded Modules:

Path |
-- |
C:\Program Files\PeaZip\res\zpaq\zpaq.exe |
C:\Windows\System32\KERNEL32.DLL |
C:\Windows\System32\KERNELBASE.dll |
C:\Windows\SYSTEM32\ntdll.dll |


## Signature

* Status: The file C:\Program Files\PeaZip\res\zpaq\zpaq.exe is not digitally signed. You cannot run this script on the current system. For more information about running scripts and setting execution policy, see about_Execution_Policies at https:/go.microsoft.com/fwlink/?LinkID=135170
* Serial: ``
* Thumbprint: ``
* Issuer: 
* Subject: 

## File Metadata

* Original Filename: 
* Product Name: 
* Company Name: 
* File Version: 
* Product Version: 
* Language: 
* Legal Copyright: 
* Machine Type: 64-bit

## File Scan

* VirusTotal Detections: 0/73
* VirusTotal Link: https://www.virustotal.com/gui/file/7a94b4f1d6323a758c7b0b6344036f166bff0fd44f1c3c86f05b3688023496cb/detection/





MIT License. Copyright (c) 2020 Strontic.


