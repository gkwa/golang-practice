<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->
Beego web framwork setup/test

- [beego intro](#beego-intro)
- [install beego on OS X](#install-beego-on-os-x)
- [install beego on Windows](#install-beego-on-windows)
- [create my new beego project](#create-my-new-beego-project)

<!-- END doctoc generated TOC please keep comment here to allow auto update -->

beego intro
===========

-   <http://beego.me/docs/install/bee.md#bee-tool-commands>
-   <https://github.com/beego/beedoc/blob/master/en-US/intro/Introduction.md>

install beego on OS X
=====================

    # Install golang
    brew install go --cross-compile-common

    # Set my personal Go workspace
    export GOPATH=$HOME/pdev/golang-practice
    export PATH=$PATH:$GOPATH/bin

    # Install Beego framework
    go get github.com/beego/bee
    cd $GOPATH/src

install beego on Windows
========================

    REM install chocolatey
    @powershell -NoProfile -ExecutionPolicy unrestricted -Command "iex ((new-object net.webclient).DownloadString('https://chocolatey.org/install.ps1'))" && set PATH=c:\chocolatey\bin;C:\ProgramData\chocolatey\bin;%PATH%
    set PATH=c:\chocolatey\bin;C:\ProgramData\chocolatey\bin;%PATH%

    REM install golang 
    REM https://chocolatey.org/packages?q=golang
    choco install golang -yes --version=1.5.1

    REM need to restart cmd.exe to get %GOROOT% into System's environment
    REM variables, (%GOROOT% evals to c:\tools\go)

    REM Set my personal Go workspace
    set GOPATH=c:\gowork
    setx GOPATH c:\gowork
    mkdir %GOPATH%
    set PATH=%PATH%;%GOPATH%\bin
    setx PATH %PATH%;%GOPATH%\bin
    go get github.com/beego/bee
    cd %GOPATH%/src

create my new beego project
===========================

    bee new myproject
    cd myproject
    bee run

Now visit <http://localhost:8080>
