

## 版本信息

+ VSCode版本vscode version：(version 1.82)
+ 已下载扩展installed extensions：

  Remote - SSH v0.106.4
  Remote - SSH: Editing Configuration Files v0.86.0
  Remote Development v0.24.0 WSL v0.81.3

## 问题简述

在vscode使用SSH连接服务器时，下载上述的几个扩展插件后，在Remote Explorer当中选择SSH target以连接服务器。但是在一些版本下下载上述扩展插件后Remote Explorer里没有SSH target选项，选择SSH tunnel后，显示通道不存在 `the tunnel isn't existed`，未能成功连接服务器。

## 解决方法

使用SSH tunnel是正确的，解决通道不存在问题的方法是在cmd中使用 `icacls "key address" /grant:r <your admin>:"(R)"`，其中 `<your admin>`需要替换成你的admin名称。

<img src="https://github.com/Sihan0229/Sihan0229.github.io/blob/master/assets/sshVScode.png?raw=true" width="100%">
