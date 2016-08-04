# powershell-snippets
A collection of handy PowerShell commands and scripts.


Check if promiscuous mode is enabled on network interface in Windows Server 2012

```
PS C:\> Get-NetAdapter | Format-List -Property ifAlias,PromiscuousMode
```

Example output:
```
ifAlias         : Management
PromiscuousMode : False

ifAlias         : Backup VLAN
PromiscuousMode : False
```

---

Count all files in a folder, including subfolders:

```
PS C:\> Get-ChildItem <folder> -File -Recurse | Measure-Object
```
