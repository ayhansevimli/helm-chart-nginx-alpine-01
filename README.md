# helm-chart-nginx-alpine-01

**********************************************************************************************************
#
# Helm Chart fot nginx-alpine-01
**********************************************************************************************************
### Clone helm-chart-nginx-alpine-01 from github
```
git clone https://github.com/ayhansevimli/helm-chart-nginx-alpine-01.git
```
```
type $env:USERPROFILE\.ssh\id_rsa.pub | ssh sdkadmin@dotnetsrv01 "cat >> .ssh/authorized_keys" ###ssh key transfer from windows
```
```
ssh sdkadmin@dotnetsrv01
```

#
### Project website-tpl-dotnetmvcproj001-freestyle-dotnetsrv01
Name
```
website-tpl-dotnetmvcproj001-freestyle-dotnetsrv01
```
GitHub Project url
```
https://github.com/ayhansevimli/website-tpl-dotnetmvcproj001.git/
```
Restrict where this project can be run / Label Expression
```
dotnetsrv01
```
Use custom workspace / Directory
```
webapp
```
Source Code Management / Git Repository URL
```
https://github.com/ayhansevimli/website-tpl-dotnetmvcproj001.git
```
Branches to build / Branch Specifier
```
main
```
:heavy_check_mark: Build Triggers / GitHub hook trigger for GITScm polling

Build Steps / Execute shell
```
