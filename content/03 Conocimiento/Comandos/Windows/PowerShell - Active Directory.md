---
tipo: comando
categoria: Windows
cursos: ["[[Administracion de Sistemas Operativos]]"]
aliases: []
tags: []
---

# PowerShell — Active Directory

```powershell
Install-WindowsFeature AD-Domain-Services -IncludeManagementTools
Install-ADDSForest -DomainName "hptecsup.local"
Get-ADUser -Filter *
New-ADOrganizationalUnit -Name "Ventas"
New-ADUser -Name "Ana Perez" -SamAccountName aperez -Path "OU=Ventas,DC=hptecsup,DC=local" -AccountPassword (Read-Host -AsSecureString) -Enabled $true
New-ADGroup -Name "TI" -GroupScope Global
Add-ADGroupMember -Identity "TI" -Members aperez
gpupdate /force
gpresult /r
```

## Red en Server Core

```powershell
New-NetIPAddress -InterfaceAlias "Ethernet0" -IPAddress 10.160.10.20 -PrefixLength 24 -DefaultGateway 10.160.10.2
Set-DnsClientServerAddress -InterfaceAlias "Ethernet0" -ServerAddresses 10.160.10.10
```

Conceptos: [[Active Directory y dominio]] · [[GPO]]
