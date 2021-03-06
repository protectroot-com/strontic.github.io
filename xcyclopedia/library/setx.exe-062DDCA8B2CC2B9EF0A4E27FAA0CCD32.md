﻿---
title: setx.exe | Setx - Sets environment variables
excerpt: What is setx.exe?
---

# setx.exe 

* File Path: `C:\windows\system32\setx.exe`
* Description: Setx - Sets environment variables

## Hashes

Type | Hash
-- | --
MD5 | `062DDCA8B2CC2B9EF0A4E27FAA0CCD32`
SHA1 | `9AC8C9ECED8027FC2392D65C0A87C5BC568EF2F1`
SHA256 | `867A772036DDDC29AC5B54DA4D6E53A1A84BF6F9DEAACFE2361DF5D9CFB8D26F`
SHA384 | `96C659FEC3676B62685D25739941A280D5A9D0603925437FBB212F72F000E712C5E6EDDBC745E5BF6334BD9A8910B246`
SHA512 | `3E0CAB178FE7BE8EA96B71C9CDE0D1A9FB2E33EE6361E4CD708FBBF7A9C0B514CB321818B68D327FAF1EA1BD843D84B3CDB7F15C988E0C5FAF1A6E60C9C26934`
SSDEEP | `1536:6DlKFuOMZVYf3wCEgGxkS90FV+qEwBZJqqd4ahF:66eVYfhkkSUsqlZJqg4ab`

## Signature

* Status: The file C:\windows\system32\setx.exe is not digitally signed. You cannot run this script on the current system. For more information about running scripts and setting execution policy, see about_Execution_Policies at http://go.microsoft.com/fwlink/?LinkID=135170
* Serial: ``
* Thumbprint: ``
* Issuer: 
* Subject: 

## File Metadata

* Original Filename: setx.exe.mui
* Product Name: Microsoft Windows Operating System
* Company Name: Microsoft Corporation
* File Version: 6.3.9600.16384 (winblue_rtm.130821-1623)
* Product Version: 6.3.9600.16384
* Language: English (United States)
* Legal Copyright:  Microsoft Corporation. All rights reserved.




## Additional Info*

**The information below is copied from [MicrosoftDocs](https://github.com/MicrosoftDocs/windowsserverdocs), which is maintained by [Microsoft](https://opensource.microsoft.com/codeofconduct/). Available under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/) license.*

---

## setx

Creates or modifies environment variables in the user or system environment, without requiring programming or scripting. The **Setx** command also retrieves the values of registry keys and writes them to text files.

> [!NOTE]
> This command provides the only command-line or programmatic way to directly and permanently set system environment values. System environment variables are manually configurable through **Control Panel** or through a registry editor. The **set** command, which is internal to the command interpreter (Cmd.exe), sets user environment variables for the current console window only.

### Syntax

```
setx [/s <computer> [/u [<domain>\]<user name> [/p [<password>]]]] <variable> <value> [/m]
setx [/s <computer> [/u [<domain>\]<user name> [/p [<password>]]]] <variable>] /k <path> [/m]
setx [/s <computer> [/u [<domain>\]<user name> [/p [<password>]]]] /f <filename> {[<variable>] {/a <X>,<Y> | /r <X>,<Y> <String>} [/m] | /x} [/d <delimiters>]
```

#### Parameters

| Parameter | Description |
|--|--|
| /s `<computer>` | Specifies the name or IP address of a remote computer. Do not use backslashes. The default value is the name of the local computer. |
| /u `[<domain>\]<user name>` | Runs the script with the credentials of the specified user account. The default value is the system permissions. |
| /p [`<password>`]| Specifies the password of the user account that is specified in the **/u** parameter. |
| `<variable>` | Specifies the name of the environment variable that you want to set. |
| `<value>` | Specifies the value to which you want to set the environment variable. |
| /k `<path>` | Specifies that the variable is set based on information from a registry key. The *path* uses the following syntax: `\\<HIVE>\<KEY>\...\<Value>`. For example, you might specify the following path: `HKEY_LOCAL_MACHINE\System\CurrentControlSet\Control\TimeZoneInformation\StandardName` |
| /f `<filename>` | Specifies the file that you want to use. |
| /a `<X>,<Y>` | Specifies absolute coordinates and offset as search parameters. |
| /r `<X>,<Y> <String>` | Specifies relative coordinates and offset from **String** as search parameters. |
| /m | Specifies to set the variable in the system environment. The default setting is the local environment. |
| /x | Displays file coordinates, ignoring the **/a**, **/r**, and **/d** command-line options. |
| /d `<delimiters>` | Specifies delimiters such as **,** or **\\** to be used in addition to the four built-in delimiters â€” SPACE, TAB, ENTER, and LINEFEED. Valid delimiters include any ASCII character. The maximum number of delimiters is 15, including built-in delimiters. |
| /? | Displays help at the command prompt. |

##### Remarks

- This command is similar to the UNIX utility SETENV.

- You can use this command to set values for user and system environment variables from one of three sources (modes): Command Line Mode, Registry Mode, or File Mode.

- This command writes variables to the master environment in the registry. Variables set with **setx** variables are available in future command windows only, not in the current command window.

- **HKEY_CURRENT_USER** and **HKEY_LOCAL_MACHINE** are the only supported hives. REG_DWORD, REG_EXPAND_SZ, REG_SZ, and REG_MULTI_SZ are the valid **RegKey** data types.

- If you gain access to **REG_MULTI_SZ** values in the registry, only the first item is extracted and used.

- You can't use this command to remove values added to the local or system environments. You can use this command with a variable name and no value to remove a corresponding value from the local environment.

- REG_DWORD registry values are extracted and used in hexadecimal mode.

- File mode supports the parsing of carriage return and line feed (CRLF) text files only.

- Running this command on an existing variable removes any variable references and uses expanded values.

  For instance, if the variable %PATH% has a reference to %JAVADIR%, and %PATH% is manipulated using **setx**, %JAVADIR% is expanded and its value is assigned directly to the target variable %PATH%. This means that future updates to %JAVADIR% **will not** be reflected in the %PATH% variable.

- Be aware there's a limit of 1024 characters when assigning contents to a variable using **setx**.

  This means that the content is cropped if you go over 1024 characters, and that the cropped text is what's applied to the target variable. If this cropped text is applied to an existing variable, it can result in loss of data previously held by the target variable.

### Examples

To set the *MACHINE* environment variable in the local environment to the value *Brand1*, type:

```
setx MACHINE Brand1
```

To set the *MACHINE* environment variable in the system environment to the value *Brand1 Computer*, type:

```
setx MACHINE Brand1 Computer /m
```

To set the *MYPATH* environment variable in the local environment to use the search path defined in the *PATH* environment variable, type:

```
setx MYPATH %PATH%
```

To set the *MYPATH* environment variable in the local environment to use the search path defined in the *PATH* environment variable after replacing **~** with **%**, type:

```
setx MYPATH ~PATH~
```

To set the *MACHINE* environment variable in the local environment to *Brand1* on a remote computer named *computer1*, type:

```
setx /s computer1 /u maindom\hiropln /p p@ssW23 MACHINE Brand1
```

To set the *MYPATH* environment variable in the local environment to use the search path defined in the *PATH* environment variable on a remote computer named *computer1*, type:

```
setx /s computer1 /u maindom\hiropln /p p@ssW23 MYPATH %PATH%
```

To set the *TZONE* environment variable in the local environment to the value found in the **HKEY_LOCAL_MACHINE\System\CurrentControlSet\Control\TimeZoneInformation\StandardName** registry key, type:

```
setx TZONE /k HKEY_LOCAL_MACHINE\System\CurrentControlSet\Control\TimeZoneInformation\StandardName
```

To set the *TZONE* environment variable in the local environment of a remote computer named *computer1* to the value found in the **HKEY_LOCAL_MACHINE\System\CurrentControlSet\Control\TimeZoneInformation\StandardName** registry key, type:

```
setx /s computer1 /u maindom\hiropln /p p@ssW23 TZONE /k HKEY_LOCAL_MACHINE\System\CurrentControlSet\Control\TimeZoneInformation\StandardName
```

To set the *BUILD* environment variable in the system environment to the value found in the **HKEY_LOCAL_MACHINE\Software\Microsoft\WindowsNT\CurrentVersion\CurrentBuildNumber** registry key, type:

```
setx BUILD /k HKEY_LOCAL_MACHINE\Software\Microsoft\WindowsNT\CurrentVersion\CurrentBuildNumber /m
```

To set the BUILD environment variable in the system environment of a remote computer named Computer1 to the value found in the **HKEY_LOCAL_MACHINE\Software\Microsoft\WindowsNT\CurrentVersion\CurrentBuildNumber** registry key, type:

```
setx /s computer1 /u maindom\hiropln /p p@ssW23  BUILD /k HKEY_LOCAL_MACHINE\Software\Microsoft\Windows NT\CurrentVersion\CurrentBuildNumber /m
```

To display the contents of a file named *Ipconfig.out*, along with the contents' corresponding coordinates, type:

```
setx /f ipconfig.out /x
```

To set the *IPADDR* environment variable in the local environment to the value found at the coordinate *5,11* in the *Ipconfig.out* file, type:

```
setx IPADDR /f ipconfig.out /a 5,11
```

To set the *OCTET1* environment variable in the local environment to the value found at the coordinate *5,3* in the *Ipconfig.out* file with delimiters **#$*.**, type:

```
setx OCTET1 /f ipconfig.out /a 5,3 /d #$*.
```

To set the *IPGATEWAY* environment variable in the local environment to the value found at the coordinate *0,7* with respect to the coordinate of *Gateway* in the *Ipconfig.out* file, type:

```
setx IPGATEWAY /f ipconfig.out /r 0,7 Gateway
```

To display the contents of the *Ipconfig.out* file, along with the contents' corresponding coordinates, on a computer named *computer1*, type:

```
setx /s computer1 /u maindom\hiropln /p p@ssW23 /f ipconfig.out /x
```

### Additional References

- [Command-Line Syntax Key](https://github.com/MicrosoftDocs/windowsserverdocs/tree/master/WindowsServerDocs/administration/windows-commands/command-line-syntax-key.md)

---



MIT License. Copyright (c) 2020 Strontic.


