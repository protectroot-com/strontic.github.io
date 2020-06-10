﻿
# verifier.exe 
* File Path: `C:\Windows\system32\verifier.exe`
* Description: Verifier Configuration Editor
* Comments: 

## Hashes
Type | Hash
-- | --
MD5 | `99EBA9BAF9E048AB6BD29148F4989672`
SHA1 | `96BBDCFE471839E46826173ECA89913F623D9B79`
SHA256 | `73ADA769002EE3D7D6EF6CBFA9F10F6E547AE229C6458E4CA66704CBC8F56FAB`
SHA384 | `F8B62E9DC77620E378F5E9F9AE07056A4B8C411888174715856CA1F52C2BECF4A8860BE63C8F741556814498B8261700`
SHA415 | `7F05468FB31FA9012C5EA793A48B8FFD1125FD7524D44C2EBCD61D8F8EF2B8BC0855044C71665C4B11FABDDF834DE8FF6181203FAA9B4635A6950B1F56375EE5`
SSDEEP | `3072:IB462C17Bc5VoJe3+Vcv2JxQQBBEB3BzefTrjqP+Oe632l+uBPMB:Iy6D7rl+u`

## Runtime Data
### Usage (stdout):
```Batchfile

Copyright (c) Microsoft Corporation. All rights reserved.

SYNTAX:

    verifier {/? | /help}
    verifier /standard /all
    verifier /standard /driver <name> [<name> ...]
    verifier /flags <options> [<options> ...] /all
    verifier /flags <options> [<options> ...] /driver <name> [<name> ...]
    verifier /rules {query | reset | default <id> | disable <id>}
    verifier /query
    verifier /querysettings
    verifier /bootmode {persistent | resetonbootfail | oneboot}
    verifier /reset
    verifier /faults [probability [pool_tags [applications [delay_minutes]]]]
    verifier /faultssystematic [<options> ...]
    verifier /log <file_name> [/interval <seconds>]
    verifier /volatile /flags <options> [<options> ...]
    verifier /volatile /adddriver <name> [<name> ...]
    verifier /volatile /removedriver <name> [<name> ...]
    verifier /volatile /faults [probability [pool_tags [applications
                [delay_minutes]]]]
    verifier /domain {wdm | ndis | ks | audio} [rules.all | rules.default ]
                /driver ... [/logging | /livedump | /onecheck]
    verifier /logging
    verifier /livedump
    verifier /onecheck

PARAMETERS:

    /? or /help
        Displays this help message.

    /standard
        Specifies standard Driver Verifier flags. This is equivalent to 
        '/flags 0x209BB'.

    /all
        Specifies that all installed drivers will be verified after the next
        boot.

    /driver <name> [<name> ...]
        Specifies one or more drivers (image names) that will be verified.
        Wildcard values (e.g. n*.sys) are not supported.

    /driver.exclude <name> [<name> ...]
        Specifies one or more drivers (image names) that will be excluded
        from verification. This parameter is applicable only if all drivers
        are selected for verification. Wildcard values (e.g. n*.sys) are not
        supported.

    /flags <options> [<options> ...]
        Specifies one or more options that should be enabled for verification.
        Flags are applied to all drivers being checked by Driver Verifier. The
        provided options values must be either in decimal, hexadecimal ("0x"
        prefix), octal ("0o" prefix) or binary ("0b" prefix) format.

        Standard Flags:
          Standard Driver Verifier options can be specified using '/standard'
          or '/flags 0x209BB'.

          0x00000001 (bit  0) - Special pool
          0x00000002 (bit  1) - Force IRQL checking
          0x00000008 (bit  3) - Pool tracking
          0x00000010 (bit  4) - I/O verification
          0x00000020 (bit  5) - Deadlock detection
          0x00000080 (bit  7) - DMA checking
          0x00000100 (bit  8) - Security checks
          0x00000800 (bit 11) - Miscellaneous checks
          0x00020000 (bit 17) - DDI compliance checking

        Additional Flags:
          These flags are intended for specific scenario testing. Flags marked
          with (*) require I/O Verification (bit 4) that will be automatically
          enabled. Flags marked with (**) support disabling of individual
          rules.

          0x00000004 (bit  2) - Randomized low resources simulation
          0x00000200 (bit  9) - Force pending I/O requests (*)
          0x00000400 (bit 10) - IRP logging (*)
          0x00002000 (bit 13) - Invariant MDL checking for stack (*)
          0x00004000 (bit 14) - Invariant MDL checking for driver (*)
          0x00008000 (bit 15) - Power framework delay fuzzing
          0x00010000 (bit 16) - Port/miniport interface checking
          0x00040000 (bit 18) - Systematic low resources simulation
          0x00080000 (bit 19) - DDI compliance checking (additional)
          0x00200000 (bit 21) - NDIS/WIFI verification (**)
          0x00800000 (bit 23) - Kernel synchronization delay fuzzing
          0x01000000 (bit 24) - VM switch verification
          0x02000000 (bit 25) - Code integrity checks

    /log.code_integrity
        This option suppresses Code Integrity violation breaks and collects
        only statistics for verified drivers. Statistics could be extracted
        via /log option or kernel debugger. This parameter is applicable only
        if Code Integrity checks are enabled.

    /rules {query | reset | default <id> | disable <id>}
        Specifies rules level control (advanced).

          query           Shows current status of controllable rules.
          reset           Resets all rules to their default state.
          default <id>    Sets rule ID to its default state.
          disable <id>    Disables specified rule ID.

    /query
        Display runtime Driver Verifier statistics and settings.

    /querysettings
        Displays a summary of the options and drivers that are currently
        enabled, or options and drivers that will be verified after the
        next boot. The display does not include drivers and options added
        using /volatile.

    /bootmode
        Specifies the Driver Verifier boot mode. This option requires system
        reboot to take effect.

          persistent        Ensures that Driver Verifier settings are
                            persistent across reboots. This is the default
                            value.
          resetonbootfail   Disables Driver Verifier for subsequent reboots
                            if the system failed to start.
          oneboot           Enables Driver Verifier only for the next boot.

    /reset
        Clears Driver Verifier flags and driver settings. This option requires
        system reboot to take effect.

    /faults [probability [pool_tags [applications [delay_minutes]]]]
        Enable the Randomized low resources simulation feature and optionally
        control parameters for the Randomized low resources simulation.

          Probability     Specifies the probability that Driver Verifier will
                          fail a given allocation. The value represents the
                          number of chances in 10,000 that Driver Verifier will
                          fail the allocation. The default value 600, means 
                          600/10000 or 6.
          Pool Tags:      Specifies a space separated list of the pool tags to
                          be injected with faults. By default, any pool
                          allocation can be injected with faults.
          Applications    Specifies a space separated list of image file names
                          (an executable) that will be injected with faults. By
                          default, any pool allocation can be injected with
                          faults.
          DelayMinutes    Specifies the number of minutes after booting during
                          which Driver Verifier does not intentionally fail any
                          allocations. This delay allows the drivers to load
                          and the system to stabilize before the test begins.
                          The default value is 8 minutes.

    /faultssystematic [<options> ...]
        Controls the Systematic low resources simulation parameters.

          enableboottime          Enables fault injections across reboots.
          disableboottime         Disables fault injections across reboots.
                                  This is the default value.
          recordboottime          Enables fault injections in 'what if' mode
                                  across reboots.
          resetboottime           Disables fault injections across reboots and
                                  clears the stack exclusion list.
          enableruntime           Dynamically enables fault injections.
          disableruntime          Dynamically disables fault injections.
          recordruntime           Dynamically enables fault injections in
                                  'what if' mode.
          resetruntime            Dynamically disables fault injections and
                                  clears the previously faulted stack list.
          querystatistics         Shows the current fault injection statistics.
          incrementcounter        Increments the test pass counter used to
                                  identify when a fault was injected.
          getstackid <counter>    Retrieves the indicated injected stack id.
          excludestack <stack_id> Excludes the stack from fault injection.

    /log <file_name> [/interval <seconds>]
        Creates a log file with the specified name and periodically writes the
        runtime statistics to this file. The interval between log file updates
        is controlled by the '/interval' parameter. The default value is 30
        seconds. Use CTRL+C to close the log and return.

    /volatile
        Changes Driver Verifier settings without rebooting the computer.
        Volatile settings take effect immediately and are in effect until the
        next system reboot.

    /volatile /adddriver <name> [<name> ...]
        Starts the verification for the specified driver or drivers.

    /volatile /removedriver <name> [<name> ...]
        Stops the verification for the specified driver or drivers.

    /domain {wdm | ndis | ks | audio} [rules.all | rules.default] /driver ...
        [/logging | /livedump | /onecheck]
        Controls the verifier extension settings. The following verifier
        extension types are supported:

          wdm               Enabled verifier extension for WDM drivers.
          ndis              Enabled verifier extension for networking drivers.
          ks                Enabled verifier extension for kernel mode
                            streaming drivers.
          audio             Enabled verifier extension for audio drivers.

        The following extension options are supported:

          rules.default     Enables default validation rules for the selected
                            verifier extension.
          rules.all         Enables all validation rules for the selected
                            verifier extension.

        /logging
          Enables logging for violated rules detected by the selected verifier
          extensions.

        /livedump
          Enables live memory dump collection for violated rules detected by
          the selected verifier extensions.

        /onecheck
          Enables reporting of violated rules only for the first instances
          detected by the selected verifier extensions.

```

### Usage (stderr):
```Batchfile

```

### Child Processes:


## Signature

* Status: Signature verified.
* Serial: 33000000BCE120FDD27CC8EE930000000000BC
* Thumbprint: E85459B23C232DB3CB94C7A56D47678F58E8E51E
* Issuer: CN=Microsoft Windows Production PCA 2011, O=Microsoft Corporation, L=Redmond, S=Washington, C=US
* Subject: CN=Microsoft Windows, O=Microsoft Corporation, L=Redmond, S=Washington, C=US

## File Metadata

* Original Filename: verifier.exe.mui
* Product Name: Microsoft Windows Operating System
* Company Name: Microsoft Corporation
* File Version: 10.0.14393.0 (rs1_release.160715-1616)
* Product Version: 10.0.14393.0
* Language: English (United States)
* Legal Copyright:  Microsoft Corporation. All rights reserved.

