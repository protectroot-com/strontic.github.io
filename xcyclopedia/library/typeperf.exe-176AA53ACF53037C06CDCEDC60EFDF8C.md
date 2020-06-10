﻿
# typeperf.exe 
* File Path: `C:\WINDOWS\SysWOW64\typeperf.exe`
* Description: Command line performance monitor
* Comments: 

## Hashes
Type | Hash
-- | --
MD5 | `176AA53ACF53037C06CDCEDC60EFDF8C`
SHA1 | `3240925E583B7C3010C6DC9A563978BD193B8C24`
SHA256 | `7222AFA59B7326736769BC835A4771248DCB3986F0F085DF200B53503D52A6B8`
SHA384 | `CC06E6473CF48235427A641A89FD21E4A131BC4048CC7110DAB1E7AAFAA795EA0C42D7139C0389773C88F69D84CD0938`
SHA415 | `5FB1E3C5D9B2113AB98F41A3C74983CA7F6BEE3878B1FCC33B3A824B0E2FD440A73CD5BEE2A9796B1A843C2878D57A9F2DDB6610F9603072B9204150AA512786`
SSDEEP | `768:mrezkicmCLTANrE9v6OIwVO87MKhNvmYUr13025roamNjAj4Qbm:m7mCQVql283vUB300MamNkjDm`

## Runtime Data
### Usage (stdout):
```Batchfile

Microsoft r TypePerf.exe (10.0.18362.1)

Typeperf writes performance data to the command window or to a log file. To
stop Typeperf, press CTRL+C.

Usage:
C:\WINDOWS\SysWOW64\typeperf.exe { <counter [counter ...]> 
                                | -cf <filename> 
                                | -q [object] 
                                | -qx [object] 
                                } [options]

Parameters:
  <counter [counter ...]>       Performance counters to monitor.

Options:
  -?                            Displays context sensitive help.
  -f <CSV|TSV|BIN|SQL>          Output file format. Default is CSV.
  -cf <filename>                File containing performance counters to
                                monitor, one per line.
  -si <[[hh:]mm:]ss>            Time between samples. Default is 1 second.
  -o <filename>                 Path of output file or SQL database. Default
                                is STDOUT.
  -q [object]                   List installed counters (no instances). To
                                list counters for one object, include the
                                object name, such as Processor.
  -qx [object]                  List installed counters with instances. To
                                list counters for one object, include the
                                object name, such as Processor.
  -sc <samples>                 Number of samples to collect. Default is to
                                sample until CTRL+C.
  -config <filename>            Settings file containing command options.
  -s <computer_name>            Server to monitor if no server is specified
                                in the counter path.
  -y                            Answer yes to all questions without prompting.

Note:
  Counter is the full name of a performance counter in
  "\\<Computer>\<Object>(<Instance>)\<Counter>" format,
  such as "\\Server1\Processor(0)\% User Time".

Examples:
  typeperf "\Processor(_Total)\% Processor Time"
  typeperf -cf counters.txt -si 5 -sc 50 -f TSV -o domain2.tsv
  typeperf -qx PhysicalDisk -o counters.txt

```

### Usage (stderr):
```Batchfile

```

### Child Processes:


## Signature

* Status: Signature verified.
* Serial: 330000023241FB59996DCC4DFF000000000232
* Thumbprint: FF82BC38E1DA5E596DF374C53E3617F7EDA36B06
* Issuer: CN=Microsoft Windows Production PCA 2011, O=Microsoft Corporation, L=Redmond, S=Washington, C=US
* Subject: CN=Microsoft Windows, O=Microsoft Corporation, L=Redmond, S=Washington, C=US

## File Metadata

* Original Filename: TypePerf.exe
* Product Name: Microsoft Windows Operating System
* Company Name: Microsoft Corporation
* File Version: 10.0.18362.1 (WinBuild.160101.0800)
* Product Version: 10.0.18362.1
* Language: English (United States)
* Legal Copyright:  Microsoft Corporation. All rights reserved.

