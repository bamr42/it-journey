---
title: Windows Sub-linux Setup
updated: 2022-05-21 23:56:40Z
created: 2024-01-16 23:01:56Z
author: null
tags:
  - article
---

If wsl is installed 

```powershell
wsl --install
wsl --update

```powershell
Invoke-WebRequest -Uri https://aka.ms/wslubuntu2004 -OutFile Ubuntu.appx -UseBasicParsing
wsl --set-default-version 2
```
