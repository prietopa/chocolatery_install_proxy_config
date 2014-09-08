chocolatery_install_proxy_config
================================

custom script from original to add proxy authentication.

**NOTE**: 
- original file from https://chocolatey.org/install.ps1
- original explanation from https://github.com/chocolatey/chocolatey/wiki/Proxy-Settings-for-Chocolatey

###1.- Download my [custom script](https://github.com/prietopa/chocolatery_install_proxy_config/blob/master/chocolater_install_proxy.ps1) to c:\install.ps1. and change:
- PROXYSERVER:PORT (line 38)
- USER (line 39)
- PASS (line 40)

Put your proxy configuration instead.

###2.- Configure PowerShell, add to console in PowerShell:

- [Environment]::SetEnvironmentVariable("http_proxy", "USER:PASS@PROXYHOST:PORT","Machine")
- [Environment]::SetEnvironmentVariable("https_proxy", "USER:PASS@PROXYHOST:PORT","Machine")

Put your proxy configuration instead.

###3.- Open PowerShell (Programs/accessories/PowerShell) and go to c:\
```
./install.ps1
```

###4.- Restart

###5.- Start to install
```
choco install atom
```
