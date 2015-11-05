<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->
Golang setup

- [beego site](#beego-site)
- [setup on OS X](#setup-on-os-x)
- [setup on Windows](#setup-on-windows)

<!-- END doctoc generated TOC please keep comment here to allow auto update -->

beego site
==========

<http://beego.me/docs/install/bee.md#bee-tool-commands>

setup on OS X
=============

    brew install go --cross-compile-common
    export GOPATH=$HOME/pdev/golang-practice
    export PATH=$PATH:$GOPATH/bin
    go get github.com/beego/bee
    cd $GOPATH/src
    bee new myproject
    cd myproject
    bee run
    # visit localhost:8080 in browser

setup on Windows
================

    REM install chocolatey
    @powershell -NoProfile -ExecutionPolicy unrestricted -Command "iex ((new-object net.webclient).DownloadString('https://chocolatey.org/install.ps1'))" && set PATH=c:\chocolatey\bin;C:\ProgramData\chocolatey\bin;%PATH%
    set PATH=c:\chocolatey\bin;C:\ProgramData\chocolatey\bin;%PATH%

    REM install golang
    choco install golang -yes --version=1.5.1

    REM need to restart cmd.exe to get %GOROOT% into System's environment
    REM variables, (%GOROOT% evals to c:\tools\go)

    set GOPATH=c:\gowork
    setx GOPATH c:\gowork
    mkdir %GOPATH%
    set PATH=%PATH%;%GOPATH%\bin
    setx PATH %PATH%;%GOPATH%\bin
    go get github.com/beego/bee
    cd %GOPATH%/src
    bee new myproject
    cd myproject
    bee run

