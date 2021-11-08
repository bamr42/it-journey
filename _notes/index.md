---
title: Notes Index
description: Notes Index
permalink: /notes/
lastmod: '2021-11-07T14:55:30.334Z'
---

# Quick Start

## [Getting Started](/notes/getting-started)

### Windows

Open Powershell in Admin mode

```shell
powershell -Command "Start-Process PowerShell -Verb RunAs"
```

Set the following environment variables:

```powershell

  $envName= 'psgist'
  $envValue= '64e4d4d22d4757be6e8e26fd39d760c9'
  $env:psgist = $envValue

function Set-EnvVar($envName, $envValue) {
    # param($envName, $envValue)
    # $env:$name = $value

[System.Environment]::    ($envName, $envValue,[System.EnvironmentVariableTarget]::User)
write-host 'Environment variable set'
write-host '$envName: $envValue'
}

Set-EnvVar $envName $envValue

echo $env:psgist


```


```powershell
$name = "amr"
$value = "smells"

function Set-LocalVar($name, $value) {
    # parm($name, $value)
    write-host "$name $value"
}

Set-LocalVar amr smells


```




[Check-Get-PS-Profile.ps1]() 

Navigate to Profile home directory

```powershell
split-path $PROFILE | cd
```
### Download $Profile

```powershell

function Git-profile {
  $gitUser ="bamr87"
  Write-Output $env:psgist
  $masterProfile = "Microsoft.PowerShell_profile.ps1"
  
  $url = "https://gist.githubusercontent.com/$gitUser/$env:psgist/raw/$masterProfile"
  $FileName = Split-Path $profile -Leaf
  $FilePath = Split-Path $profile
  $FullPath = "$FilePath\$FileName"
  
  $webclient = New-Object System.Net.WebClient
  $webclient.DownloadFile($url,$FullPath)
}

function Restart-Powershell {
  Start-Process powershell
  exit
}

```
restart  powershell function
```powershell
function Restart-Powershell {
  Start-Process powershell
  exit
}
```

### Linux


### MacOS


```javascript
document.write('Hello, world!');
```


```powershell
vscode://file/C:/Users/AmrAbdel-Motaleb/OneDrive/Documents/GitHub/{{ page.path}}
```
```bash
code $HOME/Github/
```

```liquid
{% raw %}
{{site.github.repository_url}}
{% endraw %}
```

```html
{%raw %}
<div class="sidebar__top">
  <a href="'''liquid{{site.github.repository_url}}'''/blob/gh-pages/{{page.name}}">
    <i class="fab fa-github-square"></i>
  </a>
  <a href="vscode://file{{ site.local_git_pc}}/{{ site.local_repo }}/{{ page.path }}">
    <i class="fas fa-laptop-code"></i>
  </a>
  <a href="vscode://file{{ site.local_git_mac}}/{{ site.local_repo }}/{{ page.path }}">
    <i class="fas fa-laptop-code"></i>
  </a>
  <a href="#page-title" class="back-to-top">{{ site.data.ui-text[site.locale].back_to_top | default: 'Back to Top' }} &uarr;</a>
</div>
{% endraw %}
```