chocolatery_install_proxy_config
================================

custom script from original to add proxy authentication.

**NOTE**: 
- original file from https://chocolatey.org/install.ps1
- original explanation from https://github.com/chocolatey/chocolatey/wiki/Proxy-Settings-for-Chocolatey

https://github.com/prietopa/chocolatery_install_proxy_config/blob/master/chocolater_install_proxy.ps1

1.- Download my custom ![alt text](https://github.com/prietopa/chocolatery_install_proxy_config/blob/master/chocolater_install_proxy.ps1 "script") to c:\install.ps1. and change:
- PROXYHOST
- PORT
- USER
- PASS
Put your proxy configuration instead.

2.- Configure PowerShell, add to console in PowerShell:
```
[Environment]::SetEnvironmentVariable("http_proxy", "USER:PASS@PROXYHOST:PORT","Machine")
[Environment]::SetEnvironmentVariable("https_proxy", "USER:PASS@PROXYHOST:PORT","Machine")
```
Put your proxy configuration instead.

3.- Open PowerShell (Programs/accessories/PowerShell) and go to c:\
```
./install.ps1
```

4. Restart
