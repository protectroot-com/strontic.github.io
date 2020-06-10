﻿
# tzutil.exe 
* File Path: `C:\WINDOWS\SysWOW64\tzutil.exe`
* Description: Windows Time Zone Utility
* Comments: 

## Hashes
Type | Hash
-- | --
MD5 | `A5E9EDD84FDA5F13CBE1AE635E1E3B14`
SHA1 | `5A5EB0554FA3A65BCD0DAB0F65BAF2DF429DBEE5`
SHA256 | `407EDD480F5061CEBE80CEB4634233CA1575546973A622306865644FDE28B531`
SHA384 | `990CED714099198080872F2A53BA27143713A1C78AD65F489EE1A5855E22C4D1368A545A1C764E2CEDFF817A59DD4DDD`
SHA415 | `42678253E796B51E233231FB41B80614F328899DFA2B7FE218520CC59CDF8E3E43890D84A6171DC8AB977A39A47EA22A2E6B782AD8A646C0E54E55E5CF38D3AD`
SSDEEP | `768:hiMwpD1KHjiPg7wsjjdmN2JcII4WUvT3IR8VWyup:hupDIHeo7wewYc9GcKVWyup`

## Runtime Data
### Usage (stdout):
```Batchfile
Windows Time Zone Utility

Usage:
TZUTIL </? | /g | /s TimeZoneID[_dstoff] | /l>

Parameters:
    /? Displays usage information.

    /g Displays the current time zone ID.

    /s TimeZoneID[_dstoff]
       Sets the current time zone using the specified time zone ID.
       The _dstoff suffix disables Daylight Saving Time adjustments
       for the time zone (where applicable).

    /l Lists all valid time zone IDs and display names. The output will
       be: 
           <display name>
           <time zone ID>

Examples:
    TZUTIL /g
    TZUTIL /s "Pacific Standard Time"
    TZUTIL /s "Pacific Standard Time_dstoff"

Remarks:
    An exit code of 0 indicates the command completed successfully.

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

* Original Filename: tzutil.exe
* Product Name: Microsoft Windows Operating System
* Company Name: Microsoft Corporation
* File Version: 10.0.18362.1 (WinBuild.160101.0800)
* Product Version: 10.0.18362.1
* Language: English (United States)
* Legal Copyright:  Microsoft Corporation. All rights reserved.

