﻿---
title: pack200.exe | OpenJDK Platform binary
excerpt: What is pack200.exe?
---

# pack200.exe 

* File Path: `C:\program files (x86)\Amazon Corretto\jdk1.8.0_265\jre\bin\pack200.exe`
* Description: OpenJDK Platform binary

## Hashes

Type | Hash
-- | --
MD5 | `0FF0267A0F8C0055F1B1AAF5198A1472`
SHA1 | `A6707533124C745775F1EE424901EA77E08D953C`
SHA256 | `64509659DFB41F485E98B2B5B8CE1606BB05C856174717648924CE6477446EC9`
SHA384 | `1282436C7A3A8ECF4C37ADE2CF2C7F74859A89E742AF1D753704C787CAA02360FD94C3BF6C31F0704EE48EDE6AE2AB04`
SHA512 | `BC6AAC2C32CA23DE2A2BFF1BB553586B1EB5BC01214FF81782D5057E78177F55049D927E92C329A54D428E1B3E587ED3546677D1D85D6BCDD2F8A3F559267F6B`
SSDEEP | `384:GpsD5hncqDmSHhV8VWee34SzvOK6jS1/4Dgf2hd:GpsTnoS/8Vbe3JOKgY/4Uf2hd`

## Runtime Data

### Usage (stdout):
```cmhg
Usage:  pack200 [-opt... | --option=value]... x.pack[.gz] y.jar

Packing Options
  -g, --no-gzip                   output a plain *.pack file with no zipping
  --gzip                          (default) post-process the pack output with gzip
  -G, --strip-debug               remove debugging attributes while packing
  -O, --no-keep-file-order        do not transmit file ordering information
  --keep-file-order               (default) preserve input file ordering
  -S{N}, --segment-limit={N}      output segment limit (default N=1Mb)
  -E{N}, --effort={N}             packing effort (default N=5)
  -H{h}, --deflate-hint={h}       transmit deflate hint: true, false, or keep (default)
  -m{V}, --modification-time={V}  transmit modtimes: latest or keep (default)
  -P{F}, --pass-file={F}          transmit the given input element(s) uncompressed
  -U{a}, --unknown-attribute={a}  unknown attribute action: error, strip, or pass (default)
  -C{N}={L}, --class-attribute={N}={L}  (user-defined attribute)
  -F{N}={L}, --field-attribute={N}={L}  (user-defined attribute)
  -M{N}={L}, --method-attribute={N}={L} (user-defined attribute)
  -D{N}={L}, --code-attribute={N}={L}   (user-defined attribute)
  -f{F}, --config-file={F}        read file F for Pack200.Packer properties
  -v, --verbose                   increase program verbosity
  -q, --quiet                     set verbosity to lowest level
  -l{F}, --log-file={F}           output to the given log file, or '-' for System.out
  -?, -h, --help                  print this message
  -V, --version                   print program version
  -J{X}                           pass option X to underlying Java VM

Notes:
  The -P, -C, -F, -M, and -D options accumulate.
  Example attribute definition:  -C SourceFile=RUH .
  Config. file properties are defined by the Pack200 API.
  For meaning of -S, -E, -H-, -m, -U values, see Pack200 API.
  Layout definitions (like RUH) are defined by JSR 200.

Repacking mode updates the JAR file with a pack/unpack cycle:
    pack200 [-r|--repack] [-opt | --option=value]... [repackedy.jar] y.jar


```

### Usage (stderr):
```cmhg
Usage:  pack200 [-opt... | --option=value]... x.pack[.gz] y.jar
(For more information, run pack200 --help .)

```

### Loaded Modules:

Path |
-- |
C:\program files (x86)\Amazon Corretto\jdk1.8.0_265\jre\bin\pack200.exe |
C:\Windows\SYSTEM32\ntdll.dll |
C:\Windows\System32\wow64.dll |
C:\Windows\System32\wow64cpu.dll |
C:\Windows\System32\wow64win.dll |


## Signature

* Status: Signature verified.
* Serial: `2F83C35B5136353D68CE9EB669FD1B0B`
* Thumbprint: `4BAD227329ADEF18F215B6475FB7948E1629B505`
* Issuer: CN=Symantec Class 3 SHA256 Code Signing CA, OU=Symantec Trust Network, O=Symantec Corporation, C=US
* Subject: CN=Amazon.com Services LLC, OU=Software Services, O=Amazon.com Services LLC, L=Seattle, S=Washington, C=US

## File Metadata

* Original Filename: pack200.exe
* Product Name: OpenJDK Platform 8
* Company Name: Amazon.com Inc.
* File Version: 8.0.2650.1
* Product Version: 8.0.2650.1
* Language: Language Neutral
* Legal Copyright: Copyright  2020


## File Similarity (ssdeep match)

File | Score
-- | --
[C:\program files (x86)\Amazon Corretto\jdk1.8.0_265\bin\javadoc.exe](javadoc.exe-60735A8E38579FDB6320851C1DE38408.md) | 71
[C:\program files (x86)\Amazon Corretto\jdk1.8.0_265\bin\jdb.exe](jdb.exe-A84E4AB77C8F90E25B6D0C916B0D25E1.md) | 61
[C:\program files (x86)\Amazon Corretto\jdk1.8.0_265\bin\orbd.exe](orbd.exe-DB61ACE931C41EF0EF48577287B3DAB8.md) | 61
[C:\program files (x86)\Amazon Corretto\jdk1.8.0_265\bin\pack200.exe](pack200.exe-2B30CC6FFE825CC181A4A3F9FDF071D7.md) | 91
[C:\program files (x86)\Amazon Corretto\jdk1.8.0_265\bin\rmiregistry.exe](rmiregistry.exe-457267F19E98514E55991A66650E25F3.md) | 74
[C:\program files (x86)\Amazon Corretto\jdk1.8.0_265\jre\bin\orbd.exe](orbd.exe-96A845462BBC79AA171FE9C03CE33766.md) | 60
[C:\program files (x86)\Amazon Corretto\jdk1.8.0_265\jre\bin\rmiregistry.exe](rmiregistry.exe-737C1DCE9C428110E1DBA54B571A5B03.md) | 72
[C:\program files (x86)\Amazon Corretto\jre8\bin\orbd.exe](orbd.exe-B8A6EDEBFC7BD2FB7A7C1C12A3DBEF24.md) | 58
[C:\program files (x86)\Amazon Corretto\jre8\bin\pack200.exe](pack200.exe-FFF71AB59824704A3826FB5C27C9C8E8.md) | 85
[C:\program files (x86)\Amazon Corretto\jre8\bin\rmiregistry.exe](rmiregistry.exe-EE9B42A4CF7692CC7F4C7C48685E9708.md) | 75




MIT License. Copyright (c) 2020 Strontic.


