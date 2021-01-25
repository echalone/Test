---
Module Name: TUN.Logging
Module Guid: eeac1534-25a5-4429-a073-17ec769525f5
Module Version: 1.2.0
Locale: en-US
---

# TUN.Logging Module
## Description
Provides easy to use file and mail logging. Documentation of module at https://github.com/echalone/TUN/blob/master/PowerShell/Modules/TUN.Logging/TUN.Logging.md
## Required Modules
* TUN.Credentials (1.1.0)
## Content
* [Description](#description)
* [Required Modules](#required-modules)
* [Content](#content)
* [TUN.Logging Cmdlets](#tun.logging-cmdlets)
  + [Get-HasLogDebug](#get-haslogdebug)
    - [SYNOPSIS](#synopsis)
    - [SYNTAX](#syntax)
    - [PARAMETERS](#parameters)
      * [-ConfigurationName](#-configurationname)
      * [CommonParameters](#commonparameters)
    - [OUTPUTS](#outputs)
  + [Get-HasLogError](#get-haslogerror)
    - [SYNOPSIS](#synopsis-1)
    - [SYNTAX](#syntax-1)
    - [PARAMETERS](#parameters-1)
      * [-ConfigurationName](#-configurationname-1)
      * [CommonParameters](#commonparameters-1)
    - [OUTPUTS](#outputs-1)
  + [Get-HasLogHost](#get-hasloghost)
    - [SYNOPSIS](#synopsis-2)
    - [SYNTAX](#syntax-2)
    - [PARAMETERS](#parameters-2)
      * [-ConfigurationName](#-configurationname-2)
      * [CommonParameters](#commonparameters-2)
    - [OUTPUTS](#outputs-2)
  + [Get-HasLogInformation](#get-hasloginformation)
    - [SYNOPSIS](#synopsis-3)
    - [SYNTAX](#syntax-3)
    - [PARAMETERS](#parameters-3)
      * [-ConfigurationName](#-configurationname-3)
      * [CommonParameters](#commonparameters-3)
    - [OUTPUTS](#outputs-3)
  + [Get-HasLogOutput](#get-haslogoutput)
    - [SYNOPSIS](#synopsis-4)
    - [SYNTAX](#syntax-4)
    - [PARAMETERS](#parameters-4)
      * [-ConfigurationName](#-configurationname-4)
      * [CommonParameters](#commonparameters-4)
    - [OUTPUTS](#outputs-4)
  + [Get-HasLogVerbose](#get-haslogverbose)
    - [SYNOPSIS](#synopsis-5)
    - [SYNTAX](#syntax-5)
    - [PARAMETERS](#parameters-5)
      * [-ConfigurationName](#-configurationname-5)
      * [CommonParameters](#commonparameters-5)
    - [OUTPUTS](#outputs-5)
  + [Get-HasLogWarning](#get-haslogwarning)
    - [SYNOPSIS](#synopsis-6)
    - [SYNTAX](#syntax-6)
    - [PARAMETERS](#parameters-6)
      * [-ConfigurationName](#-configurationname-6)
      * [CommonParameters](#commonparameters-6)
    - [OUTPUTS](#outputs-6)
  + [Get-HasMailLogDebug](#get-hasmaillogdebug)
    - [SYNOPSIS](#synopsis-7)
    - [SYNTAX](#syntax-7)
    - [OUTPUTS](#outputs-7)
  + [Get-HasMailLogError](#get-hasmaillogerror)
    - [SYNOPSIS](#synopsis-8)
    - [SYNTAX](#syntax-8)
    - [PARAMETERS](#parameters-7)
      * [-ConfigurationName](#-configurationname-7)
      * [CommonParameters](#commonparameters-7)
    - [OUTPUTS](#outputs-8)
  + [Get-HasMailLogHost](#get-hasmailloghost)
    - [SYNOPSIS](#synopsis-9)
    - [SYNTAX](#syntax-9)
    - [OUTPUTS](#outputs-9)
  + [Get-HasMailLogInformation](#get-hasmailloginformation)
    - [SYNOPSIS](#synopsis-10)
    - [SYNTAX](#syntax-10)
    - [OUTPUTS](#outputs-10)
  + [Get-HasMailLogOutput](#get-hasmaillogoutput)
    - [SYNOPSIS](#synopsis-11)
    - [SYNTAX](#syntax-11)
    - [OUTPUTS](#outputs-11)
  + [Get-HasMailLogVerbose](#get-hasmaillogverbose)
    - [SYNOPSIS](#synopsis-12)
    - [SYNTAX](#syntax-12)
    - [OUTPUTS](#outputs-12)
  + [Get-HasMailLogWarning](#get-hasmaillogwarning)
    - [SYNOPSIS](#synopsis-13)
    - [SYNTAX](#syntax-13)
    - [OUTPUTS](#outputs-13)
  + [Get-TUNLoggingVersion](#get-tunloggingversion)
    - [SYNOPSIS](#synopsis-14)
    - [SYNTAX](#syntax-14)
    - [PARAMETERS](#parameters-8)
      * [-AsString](#-asstring)
      * [CommonParameters](#commonparameters-8)
    - [OUTPUTS](#outputs-14)
  + [Send-Log](#send-log)
    - [SYNOPSIS](#synopsis-15)
    - [SYNTAX](#syntax-15)
    - [PARAMETERS](#parameters-9)
      * [-From](#-from)
      * [-To](#-to)
      * [-SmtpServer](#-smtpserver)
      * [-Subject](#-subject)
      * [-ConfigurationName](#-configurationname-8)
      * [-AttachLogFileConfigurations](#-attachlogfileconfigurations)
      * [-UserName](#-username)
      * [-Password](#-password)
      * [-UseSsl](#-usessl)
      * [-AlwaysSend](#-alwayssend)
      * [-SendOnError](#-sendonerror)
      * [-SendOnHost](#-sendonhost)
      * [-SendOnOutput](#-sendonoutput)
      * [-SendOnVerbose](#-sendonverbose)
      * [-SendOnWarning](#-sendonwarning)
      * [-SendOnDebug](#-sendondebug)
      * [-SendOnInformation](#-sendoninformation)
      * [-AttachLogfile](#-attachlogfile)
      * [-KeepLogging](#-keeplogging)
      * [-WhatIf](#-whatif)
      * [-Confirm](#-confirm)
      * [CommonParameters](#commonparameters-9)
    - [OUTPUTS](#outputs-15)
    - [NOTES](#notes)
  + [Set-ForceLogSend](#set-forcelogsend)
    - [SYNOPSIS](#synopsis-16)
    - [SYNTAX](#syntax-16)
    - [PARAMETERS](#parameters-10)
      * [-Reason](#-reason)
      * [-ConfigurationName](#-configurationname-9)
      * [CommonParameters](#commonparameters-10)
    - [OUTPUTS](#outputs-16)
  + [Set-LogFallbackConsoleColors](#set-logfallbackconsolecolors)
    - [SYNOPSIS](#synopsis-17)
    - [SYNTAX](#syntax-17)
    - [DESCRIPTION](#description-1)
    - [PARAMETERS](#parameters-11)
      * [-FallbackForegroundColor](#-fallbackforegroundcolor)
      * [-FallbackBackgroundColor](#-fallbackbackgroundcolor)
      * [-WhatIf](#-whatif-1)
      * [-Confirm](#-confirm-1)
      * [CommonParameters](#commonparameters-11)
    - [OUTPUTS](#outputs-17)
  + [Set-MailLogCredentials](#set-maillogcredentials)
    - [SYNOPSIS](#synopsis-18)
    - [SYNTAX](#syntax-18)
    - [DESCRIPTION](#description-2)
    - [PARAMETERS](#parameters-12)
      * [-ConfigurationName](#-configurationname-10)
      * [-CredentialsFile](#-credentialsfile)
      * [-InitCredentials](#-initcredentials)
      * [-WhatIf](#-whatif-2)
      * [-Confirm](#-confirm-2)
      * [CommonParameters](#commonparameters-12)
    - [OUTPUTS](#outputs-18)
    - [NOTES](#notes-1)
  + [Set-TUNLogging_LocalMode](#set-tunlogging_localmode)
    - [SYNOPSIS](#synopsis-19)
    - [SYNTAX](#syntax-19)
    - [PARAMETERS](#parameters-13)
      * [-Global](#-global)
      * [CommonParameters](#commonparameters-13)
    - [OUTPUTS](#outputs-19)
  + [Start-Log](#start-log)
    - [SYNOPSIS](#synopsis-20)
    - [SYNTAX](#syntax-20)
    - [DESCRIPTION](#description-3)
    - [PARAMETERS](#parameters-14)
      * [-LogPath](#-logpath)
      * [-LogName](#-logname)
      * [-LogExtension](#-logextension)
      * [-ConfigurationName](#-configurationname-11)
      * [-LogPreference_LogError](#-logpreference_logerror)
      * [-LogPreference_LogHost](#-logpreference_loghost)
      * [-LogPreference_LogOutput](#-logpreference_logoutput)
      * [-LogPreference_LogVerbose](#-logpreference_logverbose)
      * [-LogPreference_LogWarning](#-logpreference_logwarning)
      * [-LogPreference_LogDebug](#-logpreference_logdebug)
      * [-LogPreference_LogInformation](#-logpreference_loginformation)
      * [-NoFileLog](#-nofilelog)
      * [-NoTextLog](#-notextlog)
      * [-NoTimestamp](#-notimestamp)
      * [-UseComputerPrefix](#-usecomputerprefix)
      * [-UseScriptPrefix](#-usescriptprefix)
      * [-UseDefaultName](#-usedefaultname)
      * [-NoDateTimeFormat](#-nodatetimeformat)
      * [-DeleteExisting](#-deleteexisting)
      * [-AsOutput](#-asoutput)
      * [-Force](#-force)
      * [-WhatIf](#-whatif-3)
      * [-Confirm](#-confirm-3)
      * [CommonParameters](#commonparameters-14)
    - [OUTPUTS](#outputs-20)
  + [Start-MailLog](#start-maillog)
    - [SYNOPSIS](#synopsis-21)
    - [SYNTAX](#syntax-21)
    - [DESCRIPTION](#description-4)
    - [PARAMETERS](#parameters-15)
      * [-ConfigurationName](#-configurationname-12)
      * [-CredentialsFile](#-credentialsfile-1)
      * [-LogPreference_MailError](#-logpreference_mailerror)
      * [-LogPreference_MailHost](#-logpreference_mailhost)
      * [-LogPreference_MailOutput](#-logpreference_mailoutput)
      * [-LogPreference_MailVerbose](#-logpreference_mailverbose)
      * [-LogPreference_MailWarning](#-logpreference_mailwarning)
      * [-LogPreference_MailDebug](#-logpreference_maildebug)
      * [-LogPreference_MailInformation](#-logpreference_mailinformation)
      * [-AddTimestamp](#-addtimestamp)
      * [-AsOutput](#-asoutput-1)
      * [-InitCredentials](#-initcredentials-1)
      * [-Force](#-force-1)
      * [-WhatIf](#-whatif-4)
      * [-Confirm](#-confirm-4)
      * [CommonParameters](#commonparameters-15)
    - [OUTPUTS](#outputs-21)
    - [NOTES](#notes-2)
  + [Stop-Log](#stop-log)
    - [SYNOPSIS](#synopsis-22)
    - [SYNTAX](#syntax-22)
    - [PARAMETERS](#parameters-16)
      * [-ConfigurationName](#-configurationname-13)
      * [-KeepLoggingFile](#-keeploggingfile)
      * [-KeepLoggingText](#-keeploggingtext)
      * [-WhatIf](#-whatif-5)
      * [-Confirm](#-confirm-5)
      * [CommonParameters](#commonparameters-16)
    - [OUTPUTS](#outputs-22)
    - [NOTES](#notes-3)
  + [Write-DebugLog](#write-debuglog)
    - [SYNOPSIS](#synopsis-23)
    - [SYNTAX](#syntax-23)
    - [PARAMETERS](#parameters-17)
      * [-Message](#-message)
      * [-ConfigurationName](#-configurationname-14)
      * [-NoOut](#-noout)
      * [-NoLog](#-nolog)
      * [-NoMail](#-nomail)
      * [-AddTimestamp](#-addtimestamp-1)
      * [-Force](#-force-2)
      * [-ForceMail](#-forcemail)
      * [-WhatIf](#-whatif-6)
      * [-Confirm](#-confirm-6)
      * [CommonParameters](#commonparameters-17)
    - [OUTPUTS](#outputs-23)
    - [NOTES](#notes-4)
  + [Write-ErrorLog](#write-errorlog)
    - [SYNOPSIS](#synopsis-24)
    - [SYNTAX](#syntax-24)
    - [EXAMPLES](#examples)
      * [EXAMPLE 1](#example-1)
      * [EXAMPLE 2](#example-2)
    - [PARAMETERS](#parameters-18)
      * [-Message](#-message-1)
      * [-Category](#-category)
      * [-Err](#-err)
      * [-ConfigurationName](#-configurationname-15)
      * [-NoOut](#-noout-1)
      * [-NoLog](#-nolog-1)
      * [-NoMail](#-nomail-1)
      * [-AddTimestamp](#-addtimestamp-2)
      * [-NoErrorDetails](#-noerrordetails)
      * [-Force](#-force-3)
      * [-ForceMail](#-forcemail-1)
      * [-WhatIf](#-whatif-7)
      * [-Confirm](#-confirm-7)
      * [CommonParameters](#commonparameters-18)
    - [OUTPUTS](#outputs-24)
    - [NOTES](#notes-5)
  + [Write-HostLog](#write-hostlog)
    - [SYNOPSIS](#synopsis-25)
    - [SYNTAX](#syntax-25)
    - [PARAMETERS](#parameters-19)
      * [-Message](#-message-2)
      * [-ConfigurationName](#-configurationname-16)
      * [-NoNewline](#-nonewline)
      * [-ForegroundColor](#-foregroundcolor)
      * [-BackgroundColor](#-backgroundcolor)
      * [-NoOut](#-noout-2)
      * [-NoLog](#-nolog-2)
      * [-NoMail](#-nomail-2)
      * [-AddTimestamp](#-addtimestamp-3)
      * [-Force](#-force-4)
      * [-ForceMail](#-forcemail-2)
      * [-WhatIf](#-whatif-8)
      * [-Confirm](#-confirm-8)
      * [CommonParameters](#commonparameters-19)
    - [OUTPUTS](#outputs-25)
    - [NOTES](#notes-6)
  + [Write-InformationLog](#write-informationlog)
    - [SYNOPSIS](#synopsis-26)
    - [SYNTAX](#syntax-26)
    - [PARAMETERS](#parameters-20)
      * [-Message](#-message-3)
      * [-ConfigurationName](#-configurationname-17)
      * [-NoOut](#-noout-3)
      * [-NoLog](#-nolog-3)
      * [-NoMail](#-nomail-3)
      * [-AddTimestamp](#-addtimestamp-4)
      * [-Force](#-force-5)
      * [-ForceMail](#-forcemail-3)
      * [-WhatIf](#-whatif-9)
      * [-Confirm](#-confirm-9)
      * [CommonParameters](#commonparameters-20)
    - [OUTPUTS](#outputs-26)
    - [NOTES](#notes-7)
  + [Write-OutputLog](#write-outputlog)
    - [SYNOPSIS](#synopsis-27)
    - [SYNTAX](#syntax-27)
    - [PARAMETERS](#parameters-21)
      * [-Message](#-message-4)
      * [-ConfigurationName](#-configurationname-18)
      * [-NoOut](#-noout-4)
      * [-NoLog](#-nolog-4)
      * [-NoMail](#-nomail-4)
      * [-AddTimestamp](#-addtimestamp-5)
      * [-Force](#-force-6)
      * [-ForceMail](#-forcemail-4)
      * [-WhatIf](#-whatif-10)
      * [-Confirm](#-confirm-10)
      * [CommonParameters](#commonparameters-21)
    - [OUTPUTS](#outputs-27)
    - [NOTES](#notes-8)
  + [Write-VerboseLog](#write-verboselog)
    - [SYNOPSIS](#synopsis-28)
    - [SYNTAX](#syntax-28)
    - [PARAMETERS](#parameters-22)
      * [-Message](#-message-5)
      * [-ConfigurationName](#-configurationname-19)
      * [-NoOut](#-noout-5)
      * [-NoLog](#-nolog-5)
      * [-NoMail](#-nomail-5)
      * [-AddTimestamp](#-addtimestamp-6)
      * [-Force](#-force-7)
      * [-ForceMail](#-forcemail-5)
      * [-WhatIf](#-whatif-11)
      * [-Confirm](#-confirm-11)
      * [CommonParameters](#commonparameters-22)
    - [OUTPUTS](#outputs-28)
    - [NOTES](#notes-9)
  + [Write-WarningLog](#write-warninglog)
    - [SYNOPSIS](#synopsis-29)
    - [SYNTAX](#syntax-29)
    - [PARAMETERS](#parameters-23)
      * [-Message](#-message-6)
      * [-ConfigurationName](#-configurationname-20)
      * [-NoOut](#-noout-6)
      * [-NoLog](#-nolog-6)
      * [-NoMail](#-nomail-6)
      * [-AddTimestamp](#-addtimestamp-7)
      * [-Force](#-force-8)
      * [-ForceMail](#-forcemail-6)
      * [-WhatIf](#-whatif-12)
      * [-Confirm](#-confirm-12)
      * [CommonParameters](#commonparameters-23)
    - [OUTPUTS](#outputs-29)
    - [NOTES](#notes-10)

## TUN.Logging Cmdlets
### Get-HasLogDebug

#### SYNOPSIS
Determines if debug messages were logged to the log file (so far).

#### SYNTAX

```
Get-HasLogDebug [[-ConfigurationName] <String[]>] [<CommonParameters>]
```

#### PARAMETERS

##### -ConfigurationName
One or more names of the configurations for which to get the information for.
Default is $null the information will be retrieved for all running configurations.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

##### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

#### OUTPUTS

True....There have been debug messages logged to the log file

False...No debug messages have yet been logged to the log file



### Get-HasLogError

#### SYNOPSIS
Determines if errors were logged to the log file (so far).

#### SYNTAX

```
Get-HasLogError [[-ConfigurationName] <String[]>] [<CommonParameters>]
```

#### PARAMETERS

##### -ConfigurationName
One or more names of the configurations for which to get the information for.
Default is $null the information will be retrieved for all running configurations.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

##### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

#### OUTPUTS

True....There have been errors logged to the log file

False...No errors have yet been logged to the log file



### Get-HasLogHost

#### SYNOPSIS
Determines if host messages were logged to the log file (so far).

#### SYNTAX

```
Get-HasLogHost [[-ConfigurationName] <String[]>] [<CommonParameters>]
```

#### PARAMETERS

##### -ConfigurationName
One or more names of the configurations for which to get the information for.
Default is $null the information will be retrieved for all running configurations.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

##### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

#### OUTPUTS

True....There have been host messages logged to the log file

False...No host messages have yet been logged to the log file



### Get-HasLogInformation

#### SYNOPSIS
Determines if information messages were logged to the log file (so far).

#### SYNTAX

```
Get-HasLogInformation [[-ConfigurationName] <String[]>] [<CommonParameters>]
```

#### PARAMETERS

##### -ConfigurationName
One or more names of the configurations for which to get the information for.
Default is $null the information will be retrieved for all running configurations.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

##### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

#### OUTPUTS

True....There have been information messages logged to the log file

False...No information messages have yet been logged to the log file



### Get-HasLogOutput

#### SYNOPSIS
Determines if output messages were logged to the log file (so far).

#### SYNTAX

```
Get-HasLogOutput [[-ConfigurationName] <String[]>] [<CommonParameters>]
```

#### PARAMETERS

##### -ConfigurationName
One or more names of the configurations for which to get the information for.
Default is $null the information will be retrieved for all running configurations.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

##### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

#### OUTPUTS

True....There have been output messages logged to the log file

False...No output messages have yet been logged to the log file



### Get-HasLogVerbose

#### SYNOPSIS
Determines if verbose messages were logged to the log file (so far).

#### SYNTAX

```
Get-HasLogVerbose [[-ConfigurationName] <String[]>] [<CommonParameters>]
```

#### PARAMETERS

##### -ConfigurationName
One or more names of the configurations for which to get the information for.
Default is $null the information will be retrieved for all running configurations.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

##### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

#### OUTPUTS

True....There have been verbose messages logged to the log file

False...No verbose messages have yet been logged to the log file



### Get-HasLogWarning

#### SYNOPSIS
Determines if warnings were logged to the log file (so far).

#### SYNTAX

```
Get-HasLogWarning [[-ConfigurationName] <String[]>] [<CommonParameters>]
```

#### PARAMETERS

##### -ConfigurationName
One or more names of the configurations for which to get the information for.
Default is $null the information will be retrieved for all running configurations.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

##### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

#### OUTPUTS

True....There have been warnings logged to the log file

False...No warnings have yet been logged to the log file



### Get-HasMailLogDebug

#### SYNOPSIS
Determines if debug messages were logged to the mail log (so far).

#### SYNTAX

```
Get-HasMailLogDebug
```

#### OUTPUTS

True....There have been debug messages logged to the mail log

False...No debug messages have yet been logged to the mail log



### Get-HasMailLogError

#### SYNOPSIS
Determines if errors were logged to the mail log (so far).

#### SYNTAX

```
Get-HasMailLogError [[-ConfigurationName] <String[]>] [<CommonParameters>]
```

#### PARAMETERS

##### -ConfigurationName
One or more names of the configurations for which to get the information for.
Default is $null the information will be retrieved for all running text configurations.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

##### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

#### OUTPUTS

True....There have been errors logged to the mail log

False...No errors have yet been logged to the mail log



### Get-HasMailLogHost

#### SYNOPSIS
Determines if host messages were logged to the mail log (so far).

#### SYNTAX

```
Get-HasMailLogHost
```

#### OUTPUTS

True....There have been host messages logged to the mail log

False...No host messages have yet been logged to the mail log



### Get-HasMailLogInformation

#### SYNOPSIS
Determines if information messages were logged to the mail log (so far).

#### SYNTAX

```
Get-HasMailLogInformation
```

#### OUTPUTS

True....There have been information messages logged to the mail log

False...No information messages have yet been logged to the mail log



### Get-HasMailLogOutput

#### SYNOPSIS
Determines if output messages were logged to the mail log (so far).

#### SYNTAX

```
Get-HasMailLogOutput
```

#### OUTPUTS

True....There have been output messages logged to the mail log

False...No output messages have yet been logged to the mail log



### Get-HasMailLogVerbose

#### SYNOPSIS
Determines if verbose messages were logged to the mail log (so far).

#### SYNTAX

```
Get-HasMailLogVerbose
```

#### OUTPUTS

True....There have been verbose messages logged to the mail log

False...No verbose messages have yet been logged to the mail log



### Get-HasMailLogWarning

#### SYNOPSIS
Determines if warnings were logged to the mail log (so far).

#### SYNTAX

```
Get-HasMailLogWarning
```

#### OUTPUTS

True....There have been warnings logged to the mail log

False...No warnings have yet been logged to the mail log



### Get-TUNLoggingVersion

#### SYNOPSIS
Returns version of current TUN.Logging module

#### SYNTAX

```
Get-TUNLoggingVersion [-AsString] [<CommonParameters>]
```

#### PARAMETERS

##### -AsString
True/Present...will return a version string
False/Absent...will return a version object

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

##### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

#### OUTPUTS

Version of TUN.Logging module



### Send-Log

#### SYNOPSIS
Stops logging process for mail log and sends the mail log text as a text mail.
Optionally attaches the file log as attachment.

#### SYNTAX

```
Send-Log [-From] <String> [-To] <String[]> [[-SmtpServer] <String>] [[-Subject] <String>]
 [[-ConfigurationName] <String>] [[-AttachLogFileConfigurations] <String[]>] [[-UserName] <String>]
 [[-Password] <SecureString>] [-UseSsl] [-AlwaysSend] [-SendOnError] [-SendOnHost] [-SendOnOutput]
 [-SendOnVerbose] [-SendOnWarning] [-SendOnDebug] [-SendOnInformation] [-AttachLogfile] [-KeepLogging]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

#### PARAMETERS

##### -From
The from email address.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

##### -To
The to email address.
Can be one or more email addresses to which the email will be sent.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

##### -SmtpServer
The SMTP server to use for sending the email.
If this parameter is not provided, the default SMTP server as defined in $PSEmailServer will be used.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: $PSEmailServer
Accept pipeline input: False
Accept wildcard characters: False
```

##### -Subject
The beginning of the subject line of the email.
Will interpret $(COMPUTERNAME) and $(SCRIPTNAME) as variables.
If not provided, will use "Notification from $(COMPUTERNAME)/$(SCRIPTNAME)" as default.
The reason for the E-Mail sending will be added to the end of the subject line (sepearted by a comma).

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

##### -ConfigurationName
One or more names of the configurations to send emails for.
The default is $null and will...
    a) Check if a DefaultMailLog configuration exists and send that
    b) If no DefaultMailLog configuration exists, will send all running text logs as their own mail

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

##### -AttachLogFileConfigurations
Will attach log files of the provided configurations, if their file logging is enabled.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

##### -UserName
The user to use for authentication at the smtp server.
Default is $null and will either use Credentials-File or current user (depending on if credentials file was provided).

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

##### -Password
The password to use for authentication at the smtp server.

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

##### -UseSsl
True/Present...Will use Ssl to connect to the smtp server

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

##### -AlwaysSend
True/Present...Will always send the email, no matter what exactly was logged.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

##### -SendOnError
True/Present...Will send the email if an error occured and was logged in the mail text.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

##### -SendOnHost
True/Present...Will send the email if an error occured and was logged in the mail text.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

##### -SendOnOutput
True/Present...Will send the email if an error occured and was logged in the mail text.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

##### -SendOnVerbose
True/Present...Will send the email if an error occured and was logged in the mail text.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

##### -SendOnWarning
True/Present...Will send the email if an error occured and was logged in the mail text.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

##### -SendOnDebug
True/Present...Will send the email if an error occured and was logged in the mail text.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

##### -SendOnInformation
True/Present...Will send the email if an error occured and was logged in the mail text.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

##### -AttachLogfile
True/Present...Will attach the log file of the configuration to the log mail if file logging was enabled for that configuration.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

##### -KeepLogging
True/Present...Will not stop the logs for which an email was sent

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

##### -WhatIf
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

##### -Confirm
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

##### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

#### OUTPUTS

None

#### NOTES
Once this function has been called, the Write-ErrorLog etc.
functions will not add any more lines to the mail log.



### Set-ForceLogSend

#### SYNOPSIS
Sets a flag to trigger the sending of the log mail as soon as Send-Log is called (no matter what messages have been logged).

#### SYNTAX

```
Set-ForceLogSend [[-Reason] <String>] [[-ConfigurationName] <String[]>] [<CommonParameters>]
```

#### PARAMETERS

##### -Reason
The reason for force sending of mail log (will be added to subject line).
If no reason is given here, "forced" will be given as reason in the subject line.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

##### -ConfigurationName
One or more names of the configurations for which to force log sending.
Default is $null and all running text configurations will be forced to send.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

##### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

#### OUTPUTS

None



### Set-LogFallbackConsoleColors

#### SYNOPSIS
Sets global fallback colors for console output (needed fox linux).

#### SYNTAX

```
Set-LogFallbackConsoleColors [[-FallbackForegroundColor] <ConsoleColor>]
 [[-FallbackBackgroundColor] <ConsoleColor>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

#### DESCRIPTION
Sets global fallback colors for console output (needed fox linux).

#### PARAMETERS

##### -FallbackForegroundColor
The fallback foreground color for the console if none was provided and the current foreground color could not be determined from the console.
The default is Gray.

```yaml
Type: ConsoleColor
Parameter Sets: (All)
Aliases:
Accepted values: Black, DarkBlue, DarkGreen, DarkCyan, DarkRed, DarkMagenta, DarkYellow, Gray, DarkGray, Blue, Green, Cyan, Red, Magenta, Yellow, White

Required: False
Position: 1
Default value: Gray
Accept pipeline input: False
Accept wildcard characters: False
```

##### -FallbackBackgroundColor
The fallback background color for the console if none was provided and the current background color could not be determined from the console.
The default is Black.

```yaml
Type: ConsoleColor
Parameter Sets: (All)
Aliases:
Accepted values: Black, DarkBlue, DarkGreen, DarkCyan, DarkRed, DarkMagenta, DarkYellow, Gray, DarkGray, Blue, Green, Cyan, Red, Magenta, Yellow, White

Required: False
Position: 2
Default value: Black
Accept pipeline input: False
Accept wildcard characters: False
```

##### -WhatIf
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

##### -Confirm
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

##### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

#### OUTPUTS

None



### Set-MailLogCredentials

#### SYNOPSIS
Sets the credentials for mail log sending.

#### SYNTAX

```
Set-MailLogCredentials [[-ConfigurationName] <String>] [-CredentialsFile] <String> [-InitCredentials] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

#### DESCRIPTION
Sets the credentials for mail log sending.

#### PARAMETERS

##### -ConfigurationName
Name of the configuration to initialize with these settings.
The default will be DefaultMailLog.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: $script:__Constant_DefaultGlobalMailLogName__
Accept pipeline input: False
Accept wildcard characters: False
```

##### -CredentialsFile
File to store mailing credentials in and read mailing credentials from (for access to the smtp server).
Information will be stored in the XML file format.
This parameter is mandatory.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

##### -InitCredentials
True/Present...The script will ask for the credentials to use for mail sending, store them in the credentials file and will then immediatly exit the script.
                Used to either set up credentials file for the first time, or change/renew the credentials in the credential file, without performing the 
                actual task by the script.
The -WhatIf switch cannot be used to make sure the script is not performing its task, because it will also prevent
                the script from saving the credentials to the credentials file.
                This switch is ignored if the CredentialsFile parameter is not provided.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

##### -WhatIf
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

##### -Confirm
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

##### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

#### OUTPUTS

None

#### NOTES
If the credentials file cannot be found, it will ask the user for the credentials and stores it in
the credential file.
For first use or to change the credentials, use the -InitCredentials switch, which will force storing new credentials
and exits the script immediately after saving the credentials without executing the rest of the script.
This is because the -WhatIf switch 
cannot be used to make sure the script is not performing its task, because it will also prevent the script from saving the credentials to 
the credentials file.



### Set-TUNLogging_LocalMode

#### SYNOPSIS
Sets local mode for TUN Logging (for backwards compatibility)

#### SYNTAX

```
Set-TUNLogging_LocalMode [-Global] [<CommonParameters>]
```

#### PARAMETERS

##### -Global
True/Present...Will use new global mode (which is activated by default, only needed to reset to global mode)
False/Absent...Will use local mode (call this function without switch to use local mode)

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

##### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

#### OUTPUTS

None



### Start-Log

#### SYNOPSIS
Starts logging process for file log.

#### SYNTAX

```
Start-Log [[-LogPath] <String>] [[-LogName] <String>] [[-LogExtension] <String>]
 [[-ConfigurationName] <String>] [[-LogPreference_LogError] <Boolean>] [[-LogPreference_LogHost] <Boolean>]
 [[-LogPreference_LogOutput] <Boolean>] [[-LogPreference_LogVerbose] <Boolean>]
 [[-LogPreference_LogWarning] <Boolean>] [[-LogPreference_LogDebug] <Boolean>]
 [[-LogPreference_LogInformation] <Boolean>] [-NoFileLog] [-NoTextLog] [-NoTimestamp] [-UseComputerPrefix]
 [-UseScriptPrefix] [-UseDefaultName] [-NoDateTimeFormat] [-DeleteExisting] [-AsOutput] [-Force] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

#### DESCRIPTION
Once this function has been called, the Write-ErrorLog etc.
functions will add lines to a log file.

#### PARAMETERS

##### -LogPath
Path to the logfile directory. 
The default value is ".\" for the current working directory.
Will interpret $(COMPUTERNAME) and $(SCRIPTNAME) as variables.
If the path does not exist yet, it will try to create it.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: .\
Accept pipeline input: False
Accept wildcard characters: False
```

##### -LogName
Name of the logfile, will be interpreted as a datetime format if NoDateTimeFormat switch is not set.
Therefore, certain (or optionally all) letters will have to be escaped with a backslash if they should
not be interpreted as a datetime format character.
If this parameter is not provided, it will behave as if -UseDefaultName switch is set.
Will interpret $(COMPUTERNAME) and $(SCRIPTNAME) as variables.
If a file with this name (or its resulting datetime format name) does not exist yet, it will try to create it.
If a file with this name (or its resulting datetime format name) already exists, it will by default append
the log messages at the end of the log file, or delete it if the switch DeleteExisting is present.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

##### -LogExtension
Extension of the logfile
The default value is "log" if not specified otherwise.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: Log
Accept pipeline input: False
Accept wildcard characters: False
```

##### -ConfigurationName
Name of the configuration to initialize with these settings.
The default will be DefaultFileLog.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: $script:__Constant_DefaultGlobalFileLogName__
Accept pipeline input: False
Accept wildcard characters: False
```

##### -LogPreference_LogError
True....Will add error messages to the file log (no matter if they are displayed or logged in the mail log)
False...Will not add error messages to the file log (no matter if they are displayed or logged in the mail log)
null or not specified...The adding of error messages depends on the AsOutput switch.
If the AsOutput switch is present,
        then error messages will only be added if they are displayed, if the AsOutput switch is absent, they will
        always be added.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

##### -LogPreference_LogHost
True....Will add host messages to the file log (no matter if they are displayed or logged in the mail log)
False...Will not add host messages to the file log (no matter if they are displayed or logged in the mail log)
null or not specified...The adding of host messages depends on the AsOutput switch.
If the AsOutput switch is present,
        then host messages will only be added if they are displayed, if the AsOutput switch is absent, they will
        always be added.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

##### -LogPreference_LogOutput
True....Will add output messages to the file log (no matter if they are displayed or logged in the mail log)
False...Will not add output messages to the file log (no matter if they are displayed or logged in the mail log)
null or not specified...The adding of output messages depends on the AsOutput switch.
If the AsOutput switch is present,
        then output messages will only be added if they are displayed, if the AsOutput switch is absent, they will
        always be added.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

##### -LogPreference_LogVerbose
True....Will add verbose messages to the file log (no matter if they are displayed or logged in the mail log)
False...Will not add verbose messages to the file log (no matter if they are displayed or logged in the mail log)
null or not specified...The adding of verbose messages depends on the AsOutput switch.
If the AsOutput switch is present,
        then verbose messages will only be added if they are displayed, if the AsOutput switch is absent, they will
        always be added.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

##### -LogPreference_LogWarning
True....Will add warning messages to the file log (no matter if they are displayed or logged in the mail log)
False...Will not add warning messages to the file log (no matter if they are displayed or logged in the mail log)
null or not specified...The adding of warning messages depends on the AsOutput switch.
If the AsOutput switch is present,
        then warning messages will only be added if they are displayed, if the AsOutput switch is absent, they will
        always be added.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

##### -LogPreference_LogDebug
True....Will add debug messages to the file log (no matter if they are displayed or logged in the mail log)
False...Will not add debug messages to the file log (no matter if they are displayed or logged in the mail log)
null or not specified...The adding of debug messages depends on the AsOutput switch.
If the AsOutput switch is present,
        then debug messages will only be added if they are displayed, if the AsOutput switch is absent, they will
        always be added.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

##### -LogPreference_LogInformation
True....Will add information messages to the file log (no matter if they are displayed or logged in the mail log)
False...Will not add information messages to the file log (no matter if they are displayed or logged in the mail log)
null or not specified...The adding of information messages depends on the AsOutput switch.
If the AsOutput switch is present,
        then information messages will only be added if they are displayed, if the AsOutput switch is absent, they will
        always be added.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: 11
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

##### -NoFileLog
True/Present...Will not store the logs in a file, this switch is mutally exclusive with the NoTextLog switch (only one of those can be provided)

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

##### -NoTextLog
True/Present...Will not store the logs in text form, this switch is mutally exclusive with the NoFileLog switch (only one of those can be provided)

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

##### -NoTimestamp
True/Present...Will not automatically add a timestamp to the beginning of each line in the log file.
                If this switch is set, use the -AddTimestamp switch on individual log calls to add a timestamp if needed.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

##### -UseComputerPrefix
True/Present...Will add the computer name in front of the log file name, followed by an underscore (will also be in front of the script name if UseScriptPrefix switch is set too)

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

##### -UseScriptPrefix
True/Present...Will add the script name in front of the log file name, followed by an underscore.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

##### -UseDefaultName
True/Present...Will ignore LogName, UseScriptPrefix, UseComputerPrefix and NoDateTimeFormat
                and use the following name for the logfile:
                $(COMPUTERNAME)_$(SCRIPTNAME)_yyyy-MM-ddTHHmmss

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

##### -NoDateTimeFormat
True/Present...Will not interprete LogName as a datetime format (and no letters will have to be escaped with backslashes)

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

##### -DeleteExisting
True/Present...Deletes an existing log file if it already exists.
Otherwise new log messages will be appended at the end of the log file.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

##### -AsOutput
True/Present...For all message types for which no LogPreference was set (or for which the LogPreference is null) the 
                message will only be added if it is displayed to the user (or would be displayed to the user if
                it is an automatic script) according to its environment variable.
False/Absent...For all message types for which no LogPreference was set (or for which the LogPreference is null) the 
                message will always be added regardless if it is displayed to the user (or would be displayed to the 
                user if it is an automatic script) according to its environment variable.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

##### -Force
True/Present...Will log regardless of -WhatIf switch of calling script
False/Absent...Will only log if -WhatIf switch is not present in calling script

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

##### -WhatIf
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

##### -Confirm
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

##### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

#### OUTPUTS

None



### Start-MailLog

#### SYNOPSIS
Starts logging process for mail log.

#### SYNTAX

```
Start-MailLog [[-ConfigurationName] <String>] [[-CredentialsFile] <String>]
 [[-LogPreference_MailError] <Boolean>] [[-LogPreference_MailHost] <Boolean>]
 [[-LogPreference_MailOutput] <Boolean>] [[-LogPreference_MailVerbose] <Boolean>]
 [[-LogPreference_MailWarning] <Boolean>] [[-LogPreference_MailDebug] <Boolean>]
 [[-LogPreference_MailInformation] <Boolean>] [-AddTimestamp] [-AsOutput] [-InitCredentials] [-Force] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

#### DESCRIPTION
Once this function has been called, the Write-ErrorLog etc.
functions will add lines to a mail text
that can later on be sent by mail with the Send-Log command.

#### PARAMETERS

##### -ConfigurationName
Name of the configuration to initialize with these settings.
The default will be DefaultMailLog.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: $script:__Constant_DefaultGlobalMailLogName__
Accept pipeline input: False
Accept wildcard characters: False
```

##### -CredentialsFile
File to store mailing credentials in and read mailing credentials from (for access to the smtp server).
Information will be stored in the XML file format.
If no path for a credentials file was provided, the credentials of the script execution will be used to connect to the smtp server.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

##### -LogPreference_MailError
True....Will add error messages to the log mail text (no matter if they are displayed or logged in the file log)
False...Will not add error messages to the log mail text (no matter if they are displayed or logged in the file log)
null or not specified...The adding of error messages depends on the AsOutput switch.
If the AsOutput switch is present,
        then error messages will only be added if they are displayed, if the AsOutput switch is absent, they will
        always be added.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

##### -LogPreference_MailHost
True....Will add host messages to the log mail text (no matter if they are displayed or logged in the file log)
False...Will not add host messages to the log mail text (no matter if they are displayed or logged in the file log)
null or not specified...The adding of host messages depends on the AsOutput switch.
If the AsOutput switch is present,
        then host messages will only be added if they are displayed, if the AsOutput switch is absent, they will
        always be added.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

##### -LogPreference_MailOutput
True....Will add output messages to the log mail text (no matter if they are displayed or logged in the file log)
False...Will not add output messages to the log mail text (no matter if they are displayed or logged in the file log)
null or not specified...The adding of output messages depends on the AsOutput switch.
If the AsOutput switch is present,
        then output messages will only be added if they are displayed, if the AsOutput switch is absent, they will
        always be added.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

##### -LogPreference_MailVerbose
True....Will add verbose messages to the log mail text (no matter if they are displayed or logged in the file log)
False...Will not add verbose messages to the log mail text (no matter if they are displayed or logged in the file log)
null or not specified...The adding of verbose messages depends on the AsOutput switch.
If the AsOutput switch is present,
        then verbose messages will only be added if they are displayed, if the AsOutput switch is absent, they will
        always be added.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

##### -LogPreference_MailWarning
True....Will add warning messages to the log mail text (no matter if they are displayed or logged in the file log)
False...Will not add warning messages to the log mail text (no matter if they are displayed or logged in the file log)
null or not specified...The adding of warning messages depends on the AsOutput switch.
If the AsOutput switch is present,
        then warning messages will only be added if they are displayed, if the AsOutput switch is absent, they will
        always be added.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

##### -LogPreference_MailDebug
True....Will add debug messages to the log mail text (no matter if they are displayed or logged in the file log)
False...Will not add debug messages to the log mail text (no matter if they are displayed or logged in the file log)
null or not specified...The adding of debug messages depends on the AsOutput switch.
If the AsOutput switch is present,
        then debug messages will only be added if they are displayed, if the AsOutput switch is absent, they will
        always be added.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

##### -LogPreference_MailInformation
True....Will add information messages to the log mail text (no matter if they are displayed or logged in the file log)
False...Will not add information messages to the log mail text (no matter if they are displayed or logged in the file log)
null or not specified...The adding of information messages depends on the AsOutput switch.
If the AsOutput switch is present,
        then information messages will only be added if they are displayed, if the AsOutput switch is absent, they will
        always be added.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

##### -AddTimestamp
True/Present...Will add a timestamp at the beginning of each line
False/Absent...Will not add a timestamp at the beginning of each line

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

##### -AsOutput
True/Present...For all message types for which no LogPreference was set (or for which the LogPreference is null) the 
                message will only be added if it is displayed to the user (or would be displayed to the user if
                it is an automatic script) according to its environment variable.
False/Absent...For all message types for which no LogPreference was set (or for which the LogPreference is null) the 
                message will always be added regardless if it is displayed to the user (or would be displayed to the 
                user if it is an automatic script) according to its environment variable.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

##### -InitCredentials
True/Present...The script will ask for the credentials to use for mail sending, store them in the credentials file and will then immediatly exit the script.
                Used to either set up credentials file for the first time, or change/renew the credentials in the credential file, without performing the 
                actual task by the script.
The -WhatIf switch cannot be used to make sure the script is not performing its task, because it will also prevent
                the script from saving the credentials to the credentials file.
                This switch is ignored if the CredentialsFile parameter is not provided.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

##### -Force
True/Present...Will log regardless of -WhatIf switch of calling script
False/Absent...Will only log if -WhatIf switch is not present in calling script

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

##### -WhatIf
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

##### -Confirm
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

##### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

#### OUTPUTS

None

#### NOTES
If the credentials file cannot be found, it will ask the user for the credentials and stores it in
the credential file.
For first use or to change the credentials, use the -InitCredentials switch, which will force storing new credentials
and exits the script immediately after saving the credentials without executing the rest of the script.
This is because the -WhatIf switch 
cannot be used to make sure the script is not performing its task, because it will also prevent the script from saving the credentials to 
the credentials file.



### Stop-Log

#### SYNOPSIS
Stops logging process for log file.

#### SYNTAX

```
Stop-Log [[-ConfigurationName] <String[]>] [-KeepLoggingFile] [-KeepLoggingText] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

#### PARAMETERS

##### -ConfigurationName
One or more names of the configurations to write to.
Default is $null and all configurations will be stopped.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

##### -KeepLoggingFile
True/Present...Will not stop file logging
False/Absent...Will stop file logging

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

##### -KeepLoggingText
True/Present...Will not stop text logging
False/Absent...Will stop text logging

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

##### -WhatIf
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

##### -Confirm
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

##### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

#### OUTPUTS

None

#### NOTES
Once this function has been called, the Write-ErrorLog etc.
functions will not add any more lines to the file log.



### Write-DebugLog

#### SYNOPSIS
Emulates Write-Debug but also logs the message in the file and mail log (if applicable)

#### SYNTAX

```
Write-DebugLog [-Message] <Object> [[-ConfigurationName] <String[]>] [-NoOut] [-NoLog] [-NoMail]
 [-AddTimestamp] [-Force] [-ForceMail] [-WhatIf] [-Confirm] [<CommonParameters>]
```

#### PARAMETERS

##### -Message
The debug message

```yaml
Type: Object
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

##### -ConfigurationName
One or more names of the configurations to which to write to.
Default is $null and the message will be written to all running log configurations.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

##### -NoOut
True/Present...Will not print the debug message to the console

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

##### -NoLog
True/Present...Will not log the debug message to the log file

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

##### -NoMail
True/Present...Will not add the debug message to the mail log

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

##### -AddTimestamp
True/Present...Will add a timestamp to each line of the message string, regardless if the -NoTimestamp flag in Start-Log was set
False/Absent...Will only add a timestamp to each line of the message string if the -NoTimestamp flag in Start-Log was not set (which is the default behaviour)

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

##### -Force
True/Present...Will write the message to the log file, regardless of the rules for debug message logging (as set on Start-Log call)
False/Absent...Will only write the message to the log file if debug message logging rules apply (as set on Start-Log call)

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

##### -ForceMail
True/Present...Will write the message to the mail log, regardless of the rules for debug message logging (as set on Start-MailLog call)
False/Absent...Will only write the message to the mail log if debug message logging rules apply (as set on Start-MailLog call)

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

##### -WhatIf
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

##### -Confirm
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

##### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

#### OUTPUTS

None (Prints debug message)

#### NOTES
Can recieve the message through pipe



### Write-ErrorLog

#### SYNOPSIS
Emulates Write-Error but also logs the error in the file and mail log (if applicable)

#### SYNTAX

```
Write-ErrorLog [[-Message] <String>] [[-Category] <ErrorCategory>] [[-Err] <ErrorRecord>]
 [[-ConfigurationName] <String[]>] [-NoOut] [-NoLog] [-NoMail] [-AddTimestamp] [-NoErrorDetails] [-Force]
 [-ForceMail] [-WhatIf] [-Confirm] [<CommonParameters>]
```

#### EXAMPLES

##### EXAMPLE 1
```
.\Update-Month.ps1 -inputpath C:\Data\January.csv
```

##### EXAMPLE 2
```
.\Update-Month.ps1 -inputpath C:\Data\January.csv -outputPath C:\Reports\2009\January.csv
```

#### PARAMETERS

##### -Message
Additional error message

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

##### -Category
Error category of type \[System.Management.Automation.ErrorCategory\] (default is NotSpecified)

```yaml
Type: ErrorCategory
Parameter Sets: (All)
Aliases:
Accepted values: NotSpecified, OpenError, CloseError, DeviceError, DeadlockDetected, InvalidArgument, InvalidData, InvalidOperation, InvalidResult, InvalidType, MetadataError, NotImplemented, NotInstalled, ObjectNotFound, OperationStopped, OperationTimeout, SyntaxError, ParserError, PermissionDenied, ResourceBusy, ResourceExists, ResourceUnavailable, ReadError, WriteError, FromStdErr, SecurityError, ProtocolError, ConnectionError, AuthenticationError, LimitsExceeded, QuotaExceeded, NotEnabled

Required: False
Position: 2
Default value: NotSpecified
Accept pipeline input: False
Accept wildcard characters: False
```

##### -Err
Error object (as recieved by catch block), can also be recieved through pipe

```yaml
Type: ErrorRecord
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

##### -ConfigurationName
One or more names of the configurations to which to write to.
Default is $null and the message will be written to all running log configurations.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

##### -NoOut
True/Present...Will not print the error message to the console

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

##### -NoLog
True/Present...Will not log the error message to the log file

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

##### -NoMail
True/Present...Will not add the error message to the mail log

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

##### -AddTimestamp
True/Present...Will add a timestamp to each line of the message string, regardless if the -NoTimestamp flag in Start-Log was set
False/Absent...Will only add a timestamp to each line of the message string if the -NoTimestamp flag in Start-Log was not set (which is the default behaviour)

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

##### -NoErrorDetails
True/Present...Will not add details of the original error object to the error message
False/Absent...Will add details of the original error object to the error message

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

##### -Force
True/Present...Will write the message to the log file, regardless of the rules for error message logging (as set on Start-Log call)
False/Absent...Will only write the message to the log file if error message logging rules apply (as set on Start-Log call)

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

##### -ForceMail
True/Present...Will write the message to the mail log, regardless of the rules for error message logging (as set on Start-MailLog call)
False/Absent...Will only write the message to the mail log if error message logging rules apply (as set on Start-MailLog call)

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

##### -WhatIf
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

##### -Confirm
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

##### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

#### OUTPUTS

None (Prints error message)

#### NOTES
Can recieve error object through pipe, example call in catch block:
catch
{
    $_ | Write-ErrorLog "Example error message"
}



### Write-HostLog

#### SYNOPSIS
Emulates Write-Host but also logs the message in the file and mail log (if applicable)

#### SYNTAX

```
Write-HostLog [-Message] <Object> [[-ConfigurationName] <String[]>] [-NoNewline]
 [-ForegroundColor <ConsoleColor>] [-BackgroundColor <ConsoleColor>] [-NoOut] [-NoLog] [-NoMail]
 [-AddTimestamp] [-Force] [-ForceMail] [-WhatIf] [-Confirm] [<CommonParameters>]
```

#### PARAMETERS

##### -Message
The host message

```yaml
Type: Object
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

##### -ConfigurationName
One or more names of the configurations to which to write to.
Default is $null and the message will be written to all running log configurations.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

##### -NoNewline
Same as NoNewline switch in Write-Host cmdlet

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

##### -ForegroundColor
Same as ForegroundColor parameter in Write-Host cmdlet (only applies to message output to console, not logging)

```yaml
Type: ConsoleColor
Parameter Sets: (All)
Aliases:
Accepted values: Black, DarkBlue, DarkGreen, DarkCyan, DarkRed, DarkMagenta, DarkYellow, Gray, DarkGray, Blue, Green, Cyan, Red, Magenta, Yellow, White

Required: False
Position: Named
Default value: (Get-ConsoleForegroundColor)
Accept pipeline input: False
Accept wildcard characters: False
```

##### -BackgroundColor
Same as BackgroundColor parameter in Write-Host cmdlet (only applies to message output to console, not logging)

```yaml
Type: ConsoleColor
Parameter Sets: (All)
Aliases:
Accepted values: Black, DarkBlue, DarkGreen, DarkCyan, DarkRed, DarkMagenta, DarkYellow, Gray, DarkGray, Blue, Green, Cyan, Red, Magenta, Yellow, White

Required: False
Position: Named
Default value: (Get-ConsoleBackgroundColor)
Accept pipeline input: False
Accept wildcard characters: False
```

##### -NoOut
True/Present...Will not print the host message to the console

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

##### -NoLog
True/Present...Will not log the host message to the log file

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

##### -NoMail
True/Present...Will not add the host message to the mail log

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

##### -AddTimestamp
True/Present...Will add a timestamp to each line of the message string, regardless if the -NoTimestamp flag in Start-Log was set
False/Absent...Will only add a timestamp to each line of the message string if the -NoTimestamp flag in Start-Log was not set (which is the default behaviour)

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

##### -Force
True/Present...Will write the message to the log file, regardless of the rules for host message logging (as set on Start-Log call)
False/Absent...Will only write the message to the log file if host message logging rules apply (as set on Start-Log call)

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

##### -ForceMail
True/Present...Will write the message to the mail log, regardless of the rules for host message logging (as set on Start-MailLog call)
False/Absent...Will only write the message to the mail log if host message logging rules apply (as set on Start-MailLog call)

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

##### -WhatIf
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

##### -Confirm
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

##### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

#### OUTPUTS

None (Prints host message)

#### NOTES
Can recieve the message through pipe



### Write-InformationLog

#### SYNOPSIS
Emulates Write-Information but also logs the message in the file and mail log (if applicable)

#### SYNTAX

```
Write-InformationLog [-Message] <Object> [[-ConfigurationName] <String[]>] [-NoOut] [-NoLog] [-NoMail]
 [-AddTimestamp] [-Force] [-ForceMail] [-WhatIf] [-Confirm] [<CommonParameters>]
```

#### PARAMETERS

##### -Message
The information message

```yaml
Type: Object
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

##### -ConfigurationName
One or more names of the configurations to which to write to.
Default is $null and the message will be written to all running log configurations.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

##### -NoOut
True/Present...Will not print the information message to the console

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

##### -NoLog
True/Present...Will not log the information message to the log file

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

##### -NoMail
True/Present...Will not add the information message to the mail log

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

##### -AddTimestamp
True/Present...Will add a timestamp to each line of the message string, regardless if the -NoTimestamp flag in Start-Log was set
False/Absent...Will only add a timestamp to each line of the message string if the -NoTimestamp flag in Start-Log was not set (which is the default behaviour)

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

##### -Force
True/Present...Will write the message to the log file, regardless of the rules for information message logging (as set on Start-Log call)
False/Absent...Will only write the message to the log file if information message logging rules apply (as set on Start-Log call)

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

##### -ForceMail
True/Present...Will write the message to the mail log, regardless of the rules for information message logging (as set on Start-MailLog call)
False/Absent...Will only write the message to the mail log if information message logging rules apply (as set on Start-MailLog call)

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

##### -WhatIf
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

##### -Confirm
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

##### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

#### OUTPUTS

None (Prints information message)

#### NOTES
Can recieve the message through pipe



### Write-OutputLog

#### SYNOPSIS
Emulates Write-Output but also logs the message in the file and mail log (if applicable)

#### SYNTAX

```
Write-OutputLog [-Message] <Object> [[-ConfigurationName] <String[]>] [-NoOut] [-NoLog] [-NoMail]
 [-AddTimestamp] [-Force] [-ForceMail] [-WhatIf] [-Confirm] [<CommonParameters>]
```

#### PARAMETERS

##### -Message
The output message

```yaml
Type: Object
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

##### -ConfigurationName
One or more names of the configurations to which to write to.
Default is $null and the message will be written to all running log configurations.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

##### -NoOut
True/Present...Will not print the output message to the console

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

##### -NoLog
True/Present...Will not log the output message to the log file

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

##### -NoMail
True/Present...Will not add the output message to the mail log

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

##### -AddTimestamp
True/Present...Will add a timestamp to each line of the message string, regardless if the -NoTimestamp flag in Start-Log was set
False/Absent...Will only add a timestamp to each line of the message string if the -NoTimestamp flag in Start-Log was not set (which is the default behaviour)

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

##### -Force
True/Present...Will write the message to the log file, regardless of the rules for output message logging (as set on Start-Log call)
False/Absent...Will only write the message to the log file if output message logging rules apply (as set on Start-Log call)

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

##### -ForceMail
True/Present...Will write the message to the mail log, regardless of the rules for output message logging (as set on Start-MailLog call)
False/Absent...Will only write the message to the mail log if output message logging rules apply (as set on Start-MailLog call)

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

##### -WhatIf
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

##### -Confirm
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

##### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

#### OUTPUTS

None (Prints output message)

#### NOTES
Can recieve the message through pipe



### Write-VerboseLog

#### SYNOPSIS
Emulates Write-Verbose but also logs the message in the file and mail log (if applicable)

#### SYNTAX

```
Write-VerboseLog [-Message] <Object> [[-ConfigurationName] <String[]>] [-NoOut] [-NoLog] [-NoMail]
 [-AddTimestamp] [-Force] [-ForceMail] [-WhatIf] [-Confirm] [<CommonParameters>]
```

#### PARAMETERS

##### -Message
The verbose message

```yaml
Type: Object
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

##### -ConfigurationName
One or more names of the configurations to which to write to.
Default is $null and the message will be written to all running log configurations.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

##### -NoOut
True/Present...Will not print the verbose message to the console

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

##### -NoLog
True/Present...Will not log the verbose message to the log file

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

##### -NoMail
True/Present...Will not add the verbose message to the mail log

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

##### -AddTimestamp
True/Present...Will add a timestamp to each line of the message string, regardless if the -NoTimestamp flag in Start-Log was set
False/Absent...Will only add a timestamp to each line of the message string if the -NoTimestamp flag in Start-Log was not set (which is the default behaviour)

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

##### -Force
True/Present...Will write the message to the log file, regardless of the rules for verbose message logging (as set on Start-Log call)
False/Absent...Will only write the message to the log file if verbose message logging rules apply (as set on Start-Log call)

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

##### -ForceMail
True/Present...Will write the message to the mail log, regardless of the rules for verbose message logging (as set on Start-MailLog call)
False/Absent...Will only write the message to the mail log if verbose message logging rules apply (as set on Start-MailLog call)

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

##### -WhatIf
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

##### -Confirm
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

##### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

#### OUTPUTS

None (Prints verbose message)

#### NOTES
Can recieve the message through pipe



### Write-WarningLog

#### SYNOPSIS
Emulates Write-Warning but also logs the message in the file and mail log (if applicable)

#### SYNTAX

```
Write-WarningLog [-Message] <Object> [[-ConfigurationName] <String[]>] [-NoOut] [-NoLog] [-NoMail]
 [-AddTimestamp] [-Force] [-ForceMail] [-WhatIf] [-Confirm] [<CommonParameters>]
```

#### PARAMETERS

##### -Message
The warning message

```yaml
Type: Object
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

##### -ConfigurationName
One or more names of the configurations to which to write to.
Default is $null and the message will be written to all running log configurations.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

##### -NoOut
True/Present...Will not print the warning message to the console

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

##### -NoLog
True/Present...Will not log the warning message to the log file

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

##### -NoMail
True/Present...Will not add the warning message to the mail log

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

##### -AddTimestamp
True/Present...Will add a timestamp to each line of the message string, regardless if the -NoTimestamp flag in Start-Log was set
False/Absent...Will only add a timestamp to each line of the message string if the -NoTimestamp flag in Start-Log was not set (which is the default behaviour)

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

##### -Force
True/Present...Will write the message to the log file, regardless of the rules for warning message logging (as set on Start-Log call)
False/Absent...Will only write the message to the log file if warning message logging rules apply (as set on Start-Log call)

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

##### -ForceMail
True/Present...Will write the message to the mail log, regardless of the rules for warning message logging (as set on Start-MailLog call)
False/Absent...Will only write the message to the mail log if warning message logging rules apply (as set on Start-MailLog call)

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

##### -WhatIf
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

##### -Confirm
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

##### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

#### OUTPUTS

None (Prints warning message)

#### NOTES
Can recieve the message through pipe



