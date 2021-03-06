---
external help file: MyUptime-help.xml
Module Name: MyUptime
online version:
schema: 2.0.0
---

# Update-MyUptime

## SYNOPSIS

Refresh a saved MyUptime object.

## SYNTAX

```yaml
Update-MyUptime [-ComputerObject] <MyUptime[]> [-Passthru] [<CommonParameters>]
```

## DESCRIPTION

If you run Get-MyUptime and save the results to a variable, some properties like Uptime won't be updated the next time you look at the variable. You can use this command to refresh or update the MyUptime objects.

## EXAMPLES

### EXAMPLE 1

```powershell
PS C:\> $b = Get-Myuptime chi-p50
PS C:\> $b | Select computername,uptime

Computername Uptime
------------ ------
CHI-P50      2.00:06:47.1523262

PS C:\> $b | Update-MyUptime
PS C:\> $b | Select computername,uptime

Computername Uptime
------------ ------
CHI-P50      2.00:07:39.4540150
```

## PARAMETERS

### -ComputerObject

A computer object created with Get-MyUptime

```yaml
Type: MyUptime[]
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Passthru

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

### CommonParameters

This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### MyUptime[]

## OUTPUTS

### MyUptime

## NOTES

Learn more about PowerShell: http://jdhitsolutions.com/blog/essential-powershell-resources/

## RELATED LINKS

[Get-MyUptime]()
