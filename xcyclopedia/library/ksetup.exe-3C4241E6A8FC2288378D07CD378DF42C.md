﻿---
title: ksetup.exe | Kerberos Setup tool
excerpt: What is ksetup.exe?
---

# ksetup.exe 

* File Path: `C:\Windows\SysWOW64\ksetup.exe`
* Description: Kerberos Setup tool

## Hashes

Type | Hash
-- | --
MD5 | `3C4241E6A8FC2288378D07CD378DF42C`
SHA1 | `207BB73474EA60F1EF2DAE901E43D789E8B29A95`
SHA256 | `83B79562A118524EF74F15B264E50AEB5307BDDA765F5413AADDB894ED742DA5`
SHA384 | `CDEC9087E4B8A30DDA89052DB6255C356BB8D842784D15099F46E9A57009ED9B3C3F89EAB3654F8A76B0D493BC86FA6C`
SHA512 | `39570A9F77D812BB5442619CC104A7C9E561C0D9D5563D23A74AED1D7A4C083C067581FCEE79AE3E5E3D33A6FBA16DC18F6968B1A4EDBAE180F00842120E3E24`
SSDEEP | `768:x0twZ+bFWzclX3uV/+YvdT7iwrZVFx4ZVrjqe6td2dIpg:xj+b4olX3C+AdT7iw1VFx4XfOtduIpg`
IMP | `EA5012A878F0C2120889BBC97F54D267`
PESHA1 | `9CC3E72235CD9B59E46FE623CCCBAB680C2D36F1`
PE256 | `39CD6B6FC45E2CD38DC694A7BBA5A9283A778E2A95CF8F689796CF323F08E9CC`

## Runtime Data

### Usage (stdout):
```cmhg

USAGE:
/SetRealm <DnsDomainName>
	Makes this computer a member of an RFC1510 Kerberos Realm
/MapUser <Principal> [Account]
	Maps a Kerberos Principal ('*' = any principal)
	to an account ('*' = an account by same name);
	If account name is omitted, mapping is deleted 
	for the specified principal
/AddKdc <RealmName> [KdcName]
	Defines a KDC entry for the given realm.
	If KdcName omitted, DNS may be used to locate KDCs.
/DelKdc <RealmName> [KdcName]
	deletes a KDC entry for the realm.
	If KdcName omitted, the realm entry itself is deleted.
/AddKpasswd <Realmname> <KpasswdName>
	Add Kpasswd server address for a realm
/DelKpasswd <Realmname> <KpasswdName>
	Delete Kpasswd server address for a realm
/Server <Servername>
	specify name of a Windows machine to target the changes.
/SetComputerPassword <Password>
	Sets the password for the computer's domain account
	(or host principal)
/RemoveRealm <RealmName>
	delete all information for this realm from the registry.
/Domain [DomainName]
	use this domain (if DomainName is unspecified, detect it)
/ChangePassword <OldPasswd> <NewPasswd>
	Use Kpasswd to change the logged-on user's password.
	Use '*' to be prompted for passwords.
/ListRealmFlags (no args)
	Lists the available Realm flags that ksetup knows
/SetRealmFlags <realm> <flag> [flag] [flag] [...]
	Sets RealmFlags for a specific realm
/AddRealmFlags <realm> <flag> [flag] [flag] [...]
	Adds additional RealmFlags to a realm
/DelRealmFlags <realm> <flag> [flag] [flag] [...]
	Deletes RealmFlags from a realm.
/DumpState (no args)
	Analyze the kerberos configuration on the given machine.
/AddHostToRealmMap <host> <realm>
	Adds a mapping for <host> to <realm> to the registry.
/DelHostToRealmMap <host> <realm>
	Deletes existing mapping for <host> to <realm> from the registry.
/SetEncTypeAttr <domainname> <enctypes>
	Sets the encryption types trust attribute for <domain> to <enctypes> (multiple types should be separated by spaces).
	Supported encryption types are:
	  DES-CBC-CRC, DES-CBC-MD5, RC4-HMAC-MD5, 
	  AES128-CTS-HMAC-SHA1-96, AES256-CTS-HMAC-SHA1-96
/GetEncTypeAttr <domainname>
	Gets the encryption types trust attribute for <domain>.
/AddEncTypeAttr <domainname> <enctypes>
	Adds <enctypes> to the encryption types trust attribute for <domain> (multiple types should be separated by spaces).
/DelEncTypeAttr <domainname>
	Deletes the encryption types trust attribute for <domain>.

```

### Loaded Modules:

Path |
-- |
C:\Windows\SYSTEM32\ntdll.dll |
C:\Windows\System32\wow64.dll |
C:\Windows\System32\wow64cpu.dll |
C:\Windows\System32\wow64win.dll |
C:\Windows\SysWOW64\ksetup.exe |


## Signature

* Status: Signature verified.
* Serial: `33000001C422B2F79B793DACB20000000001C4`
* Thumbprint: `AE9C1AE54763822EEC42474983D8B635116C8452`
* Issuer: CN=Microsoft Windows Production PCA 2011, O=Microsoft Corporation, L=Redmond, S=Washington, C=US
* Subject: CN=Microsoft Windows, O=Microsoft Corporation, L=Redmond, S=Washington, C=US

## File Metadata

* Original Filename: ksetup.exe.mui
* Product Name: Microsoft Windows Operating System
* Company Name: Microsoft Corporation
* File Version: 10.0.17763.1 (WinBuild.160101.0800)
* Product Version: 10.0.17763.1
* Language: English (United States)
* Legal Copyright:  Microsoft Corporation. All rights reserved.
* Machine Type: 32-bit

## File Scan

* VirusTotal Detections: 0/64
* VirusTotal Link: https://www.virustotal.com/gui/file/83b79562a118524ef74f15b264e50aeb5307bdda765f5413aaddb894ed742da5/detection/



## Additional Info*

**The information below is copied from [MicrosoftDocs](https://github.com/MicrosoftDocs/windowsserverdocs), which is maintained by [Microsoft](https://opensource.microsoft.com/codeofconduct/). Available under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/) license.*

---

## ksetup

Performs tasks related to setting up and maintaining Kerberos protocol and the Key Distribution Center (KDC) to support Kerberos realms. Specifically, this command is used to:

- Change the computer settings for locating Kerberos realms. In non-Microsoft, Kerberosâ€“based implementations, this information is usually kept in the Krb5.conf file. In Windows Server operating systems, it's kept in the registry. You can use this tool to modify these settings. These settings are used by workstations to locate Kerberos realms and by domain controllers to locate Kerberos realms for cross-realm trust relationships.

- Initialize registry keys that the Kerberos Security Support Provider (SSP) uses to locate a KDC for the Kerberos realm, if the computer is isn't a member of a Windows domain. After configuration, the user of a client computer running the Windows operating system can log on to accounts in the Kerberos realm.

- Search the registry for the domain name of the user's realm and then resolves the name to an IP address by querying a DNS server. The Kerberos protocol can use DNS to locate KDCs by using only the realm name, but it must be specially configured to do so.

### Syntax

```
ksetup
[/setrealm <DNSdomainname>]
[/mapuser <principal> <account>]
[/addkdc <realmname> <KDCname>]
[/delkdc <realmname> <KDCname>]
[/addkpasswd <realmname> <KDCPasswordName>]
[/delkpasswd <realmname> <KDCPasswordName>]
[/server <servername>]
[/setcomputerpassword <password>]
[/removerealm <realmname>]
[/domain <domainname>]
[/changepassword <oldpassword> <newpassword>]
[/listrealmflags]
[/setrealmflags <realmname> [sendaddress] [tcpsupported] [delegate] [ncsupported] [rc4]]
[/addrealmflags <realmname> [sendaddress] [tcpsupported] [delegate] [ncsupported] [rc4]]
[/delrealmflags [sendaddress] [tcpsupported] [delegate] [ncsupported] [rc4]]
[/dumpstate]
[/addhosttorealmmap] <hostname> <realmname>]
[/delhosttorealmmap] <hostname> <realmname>]
[/setenctypeattr] <domainname> {DES-CBC-CRC | DES-CBC-MD5 | RC4-HMAC-MD5 | AES128-CTS-HMAC-SHA1-96 | AES256-CTS-HMAC-SHA1-96}
[/getenctypeattr] <domainname>
[/addenctypeattr] <domainname> {DES-CBC-CRC | DES-CBC-MD5 | RC4-HMAC-MD5 | AES128-CTS-HMAC-SHA1-96 | AES256-CTS-HMAC-SHA1-96}
[/delenctypeattr] <domainname>
```

#### Parameters

| Parameter | Description |
| --------- | ----------- |
| [ksetup setrealm](https://github.com/MicrosoftDocs/windowsserverdocs/tree/master/WindowsServerDocs/administration/windows-commands/ksetup-setrealm.md) | Makes this computer a member of a Kerberos realm. |
| [ksetup addkdc](https://github.com/MicrosoftDocs/windowsserverdocs/tree/master/WindowsServerDocs/administration/windows-commands/ksetup-addkdc.md) | Defines a KDC entry for the given realm. |
| [ksetup delkdc](https://github.com/MicrosoftDocs/windowsserverdocs/tree/master/WindowsServerDocs/administration/windows-commands/ksetup-delkdc.md) | Deletes a KDC entry for the realm. |
| [ksetup addkpasswd](https://github.com/MicrosoftDocs/windowsserverdocs/tree/master/WindowsServerDocs/administration/windows-commands/ksetup-addkpasswd.md) | Adds a kpasswd server address for a realm. |
| [ksetup delkpasswd](https://github.com/MicrosoftDocs/windowsserverdocs/tree/master/WindowsServerDocs/administration/windows-commands/ksetup-delkpasswd.md) | Deletes a kpasswd server address for a realm. |
| [ksetup server](https://github.com/MicrosoftDocs/windowsserverdocs/tree/master/WindowsServerDocs/administration/windows-commands/ksetup-server.md) | Allows you to specify the name of a Windows computer on which to apply the changes. |
| [ksetup setcomputerpassword](https://github.com/MicrosoftDocs/windowsserverdocs/tree/master/WindowsServerDocs/administration/windows-commands/ksetup-setcomputerpassword.md) | Sets the password for the computer's domain account (or host principal). |
| [ksetup removerealm](https://github.com/MicrosoftDocs/windowsserverdocs/tree/master/WindowsServerDocs/administration/windows-commands/ksetup-removerealm.md) | Deletes all information for the specified realm from the registry. |
| [ksetup domain](https://github.com/MicrosoftDocs/windowsserverdocs/tree/master/WindowsServerDocs/administration/windows-commands/ksetup-domain.md) | Allows you to specify a domain (if the `<domainname>` hasn't already been set by the **/domain** parameter). |
| [ksetup changepassword](https://github.com/MicrosoftDocs/windowsserverdocs/tree/master/WindowsServerDocs/administration/windows-commands/ksetup-changepassword.md) | Allows you to use the kpasswd to change the logged on user's password. |
| [ksetup listrealmflags](https://github.com/MicrosoftDocs/windowsserverdocs/tree/master/WindowsServerDocs/administration/windows-commands/ksetup-listrealmflags.md) | Lists the available realm flags that **ksetup** can detect. |
| [ksetup setrealmflags](https://github.com/MicrosoftDocs/windowsserverdocs/tree/master/WindowsServerDocs/administration/windows-commands/ksetup-setrealmflags.md) | Sets realm flags for a specific realm. |
| [ksetup addrealmflags](https://github.com/MicrosoftDocs/windowsserverdocs/tree/master/WindowsServerDocs/administration/windows-commands/ksetup-addrealmflags.md) | Adds additional realm flags to a realm. |
| [ksetup delrealmflags](https://github.com/MicrosoftDocs/windowsserverdocs/tree/master/WindowsServerDocs/administration/windows-commands/ksetup-delrealmflags.md) | Deletes realm flags from a realm. |
| [ksetup dumpstate](https://github.com/MicrosoftDocs/windowsserverdocs/tree/master/WindowsServerDocs/administration/windows-commands/ksetup-dumpstate.md) | Analyzes the Kerberos configuration on the given computer. Adds a host to realm mapping to the registry. |
| [ksetup addhosttorealmmap](https://github.com/MicrosoftDocs/windowsserverdocs/tree/master/WindowsServerDocs/administration/windows-commands/ksetup-addhosttorealmmap.md) | Adds a registry value to map the host to the Kerberos realm. |
| [ksetup delhosttorealmmap](https://github.com/MicrosoftDocs/windowsserverdocs/tree/master/WindowsServerDocs/administration/windows-commands/ksetup-delhosttorealmmap.md) | Deletes the registry value that mapped the host computer to the Kerberos realm. |
| [ksetup setenctypeattr](https://github.com/MicrosoftDocs/windowsserverdocs/tree/master/WindowsServerDocs/administration/windows-commands/ksetup-setenctypeattr.md) | Sets one or more encryption types trust attributes for the domain. |
| [ksetup getenctypeattr](https://github.com/MicrosoftDocs/windowsserverdocs/tree/master/WindowsServerDocs/administration/windows-commands/ksetup-getenctypeattr.md) | Gets the encryption types trust attribute for the domain. |
| [ksetup addenctypeattr](https://github.com/MicrosoftDocs/windowsserverdocs/tree/master/WindowsServerDocs/administration/windows-commands/ksetup-addenctypeattr.md) | Adds encryption types to the encryption types trust attribute for the domain. |
| [ksetup delenctypeattr](https://github.com/MicrosoftDocs/windowsserverdocs/tree/master/WindowsServerDocs/administration/windows-commands/ksetup-delenctypeattr.md) | Deletes the encryption types trust attribute for the domain. |
| /? | Displays Help at the command prompt. |

### Additional References

- [Command-Line Syntax Key](https://github.com/MicrosoftDocs/windowsserverdocs/tree/master/WindowsServerDocs/administration/windows-commands/command-line-syntax-key.md)

---



MIT License. Copyright (c) 2020 Strontic.


