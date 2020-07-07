﻿---
title: choice.exe | Offers the user a choice
---

# choice.exe 

* File Path: `C:\Windows\system32\choice.exe`
* Description: Offers the user a choice
* Comments: 

## Hashes

Type | Hash
-- | --
MD5 | `1A9804F0C374283B094E9E55DC5EE128`
SHA1 | `145F6745C02F5EFA23A411B5F87FCC995A4D3856`
SHA256 | `B2191C32538842D3FDEFF972E5A77527FA35D69FA400AAD2AA2798B86FC6CF2A`
SHA384 | `6B3CEFC5C85C090D77BD00D8900C7233A53CAC450111DA1E9634AC2ACD220B73AD0EC7B92DBA2CE0F3035E40E96B9559`
SHA512 | `8CE31A84D01204F8360F75904500C9AE26218BF4E0A1A6F97108EDB65B20FE857FE597438BE5068AE0C7CB6F8A0F417039B19709BF8CC8D441FCB4DBFCA7CC62`
SSDEEP | `768:PZPyoiiumgQlRXh66ANl3HrGq9dyCq41Ar/27V1ZUxGt3P:VPbu/3HTdyCq41Ar/61qxS3P`

## Runtime Data

### Usage (stdout):
```Batchfile

CHOICE [/C choices] [/N] [/CS] [/T timeout /D choice] [/M text]

Description:
    This tool allows users to select one item from a list 
    of choices and returns the index of the selected choice.

Parameter List:
   /C    choices       Specifies the list of choices to be created.
                       Default list is "YN".

   /N                  Hides the list of choices in the prompt.
                       The message before the prompt is displayed
                       and the choices are still enabled.

   /CS                 Enables case-sensitive choices to be selected.
                       By default, the utility is case-insensitive.

   /T    timeout       The number of seconds to pause before a default 
                       choice is made. Acceptable values are from 0 to 
                       9999. If 0 is specified, there will be no pause 
                       and the default choice is selected.

   /D    choice        Specifies the default choice after nnnn seconds.
                       Character must be in the set of choices specified
                       by /C option and must also specify nnnn with /T.

   /M    text          Specifies the message to be displayed before 
                       the prompt. If not specified, the utility 
                       displays only a prompt.

   /?                  Displays this help message.

   NOTE:
   The ERRORLEVEL environment variable is set to the index of the
   key that was selected from the set of choices. The first choice
   listed returns a value of 1, the second a value of 2, and so on.
   If the user presses a key that is not a valid choice, the tool 
   sounds a warning beep. If tool detects an error condition,
   it returns an ERRORLEVEL value of 255. If the user presses 
   CTRL+BREAK or CTRL+C, the tool returns an ERRORLEVEL value
   of 0. When you use ERRORLEVEL parameters in a batch program, list
   them in decreasing order.

Examples:
   CHOICE /?
   CHOICE /C YNC /M "Press Y for Yes, N for No or C for Cancel."
   CHOICE /T 10 /C ync /CS /D y 
   CHOICE /C ab /M "Select a for option 1 and b for option 2."
   CHOICE /C ab /N /M "Select a for option 1 and b for option 2."

```

### Usage (stderr):
```Batchfile
ERROR: Invalid argument/option - '-help'.
Type "CHOICE /?" for usage.

```

### Child Processes:


## Signature

* Status: Signature verified.
* Serial: `3300000266BD1580EFA75CD6D3000000000266`
* Thumbprint: `A4341B9FD50FB9964283220A36A1EF6F6FAA7840`
* Issuer: CN=Microsoft Windows Production PCA 2011, O=Microsoft Corporation, L=Redmond, S=Washington, C=US
* Subject: CN=Microsoft Windows, O=Microsoft Corporation, L=Redmond, S=Washington, C=US

## File Metadata

* Original Filename: choice.exe.mui
* Product Name: Microsoft Windows Operating System
* Company Name: Microsoft Corporation
* File Version: 10.0.19041.1 (WinBuild.160101.0800)
* Product Version: 10.0.19041.1
* Language: English (United States)
* Legal Copyright:  Microsoft Corporation. All rights reserved.


## Possible Misuse

*The following table contains possible examples of `choice.exe` being misused. While `choice.exe` is **not** inherently malicious, its legitimate functionality can by abused for malicious purposes.*

Source | Source File | Example | License
-- | -- | -- | --
[LOLBAS](https://github.com/LOLBAS-Project/LOLBAS) | [Wab.yml](https://github.com/LOLBAS-Project/LOLBAS/blob/master/yml/OSBinaries/Wab.yml) | `    Description: Change HKLM\Software\Microsoft\WAB\DLLPath and execute DLL of choice` | 
[atomic-red-team](https://github.com/redcanaryco/atomic-red-team) | [index.md](https://github.com/redcanaryco/atomic-red-team/blob/master/atomics/Indexes/Indexes-Markdown/index.md) |   - Atomic Test #3: Maldoc choice flags command execution [windows] | [MIT License. © 2018 Red Canary](https://github.com/redcanaryco/atomic-red-team/blob/master/LICENSE.txt)
[atomic-red-team](https://github.com/redcanaryco/atomic-red-team) | [windows-index.md](https://github.com/redcanaryco/atomic-red-team/blob/master/atomics/Indexes/Indexes-Markdown/windows-index.md) |   - Atomic Test #3: Maldoc choice flags command execution [windows] | [MIT License. © 2018 Red Canary](https://github.com/redcanaryco/atomic-red-team/blob/master/LICENSE.txt)
[atomic-red-team](https://github.com/redcanaryco/atomic-red-team) | [T1204.002.md](https://github.com/redcanaryco/atomic-red-team/blob/master/atomics/T1204.002/T1204.002.md) | - [Atomic Test #3 - Maldoc choice flags command execution](#atomic-test-3---maldoc-choice-flags-command-execution) | [MIT License. © 2018 Red Canary](https://github.com/redcanaryco/atomic-red-team/blob/master/LICENSE.txt)
[atomic-red-team](https://github.com/redcanaryco/atomic-red-team) | [T1204.002.md](https://github.com/redcanaryco/atomic-red-team/blob/master/atomics/T1204.002/T1204.002.md) | ## Atomic Test #3 - Maldoc choice flags command execution | [MIT License. © 2018 Red Canary](https://github.com/redcanaryco/atomic-red-team/blob/master/LICENSE.txt)
[atomic-red-team](https://github.com/redcanaryco/atomic-red-team) | [T1204.002.md](https://github.com/redcanaryco/atomic-red-team/blob/master/atomics/T1204.002/T1204.002.md) | $macrocode = "  a = Shell(`"cmd.exe /c choice /C Y /N /D Y /T 3`", vbNormalFocus)" | [MIT License. © 2018 Red Canary](https://github.com/redcanaryco/atomic-red-team/blob/master/LICENSE.txt)
[atomic-red-team](https://github.com/redcanaryco/atomic-red-team) | [python](https://github.com/redcanaryco/atomic-red-team/blob/master/execution-frameworks/contrib/python/README.md) | - Try to run the script: "python runner.py interactive".  Try to run the technique of your choice. | [MIT License. © 2018 Red Canary](https://github.com/redcanaryco/atomic-red-team/blob/master/LICENSE.txt)

## Additional Info*

**The information below is copied from [MicrosoftDocs](https://github.com/MicrosoftDocs/windowsserverdocs), which is maintained by [Microsoft](https://opensource.microsoft.com/codeofconduct/). Available under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/) license.*

---

## choice

Prompts the user to select one item from a list of single-character choices in a batch program, and then returns the index of the selected choice. If used without parameters, **choice** displays the default choices **Y** and **N**.

### Syntax

```
choice [/c [<choice1><choice2><â€¦>]] [/n] [/cs] [/t <timeout> /d <choice>] [/m <text>]
```

#### Parameters

| Parameter | Description |
| --------- | ----------- |
| /c `<choice1><choice2><â€¦>` | Specifies the list of choices to be created. Valid choices include a-z, A-Z, 0-9, and extended ASCII characters (128-254). The default list is YN, which is displayed as `[Y,N]?`. |
| /n | Hides the list of choices, although the choices are still enabled and the message text (if specified by **/m**) is still displayed. |
| /cs | Specifies that the choices are case-sensitive. By default, the choices are not case-sensitive. |
| /t `<timeout>` | Specifies the number of seconds to pause before using the default choice specified by **/d**. Acceptable values are from **0** to **9999**. If **/t** is set to **0**, **choice** does not pause before returning the default choice. |
| /d `<choice>` | Specifies the default choice to use after waiting the number of seconds specified by **/t**. The default choice must be in the list of choices specified by **/c**. |
| /m `<text>` | Specifies a message to display before the list of choices. If **/m** is not specified, only the choice prompt is displayed. |
| /? | Displays help at the command prompt. |

### Remarks

- The **ERRORLEVEL** environment variable is set to the index of the key that the user selects from the list of choices. The first choice in the list returns a value of `1`, the second a value of `2`, and so on. If the user presses a key that is not a valid choice, **choice** sounds a warning beep.

- If **choice** detects an error condition, it returns an **ERRORLEVEL** value of `255`. If the user presses CTRL+BREAK or CTRL+C, **choice** returns an **ERRORLEVEL** value of `0`.

> [!NOTE]
> When you use **ERRORLEVEL** values in a batch program, you must list them in decreasing order.

### Examples

To present the choices **Y**, **N**, and **C**, type the following line in a batch file:

```
choice /c ync
```

The following prompt appears when the batch file runs the **choice** command:

```
[Y,N,C]?
```

To hide the choices **Y**, **N**, and **C**, but display the text **Yes**, **No**, or **Continue**, type the following line in a batch file:

```
choice /c ync /n /m Yes, No, or Continue?
```

> [!NOTE]
> If you use the **/n** parameter, but do not use **/m**, the user is not prompted when **choice** is waiting for input.

To show both the text and the options used in the previous examples, type the following line in a batch file:

```
choice /c ync /m Yes, No, or Continue
```

To set a time limit of five seconds and specify **N** as the default value, type the following line in a batch file:

```
choice /c ync /t 5 /d n
```

> [!NOTE]
> In this example, if the user doesn't press a key within five seconds, **choice** selects **N** by default and returns an error value of `2`. Otherwise, **choice** returns the value corresponding to the user's choice.

### Additional References

- [Command-Line Syntax Key](https://github.com/MicrosoftDocs/windowsserverdocs/tree/master/WindowsServerDocs/administration/windows-commands/command-line-syntax-key.md)

---



MIT License. Copyright (c) 2020 Strontic.

