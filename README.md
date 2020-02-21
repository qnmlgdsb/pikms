##pikms是什么?
一个树莓派变成KMS的东东，找到大佬编好的程序，运行制定版本

向
https://github.com/Wind4/vlmcsd
致敬

##pikms有哪些功能？

* 树莓派的KMS化


##有问题反馈
在使用中有任何问题，欢迎反馈给我，可以用以下联系方式跟我交流


##捐助开发者
在兴趣的驱动下,写一个`免费`的东西，有欣喜，也还有汗水，希望你喜欢我的作品，同时也能支持一下。
当然，有钱捧个钱场（右上角的爱心标志，支持支付宝和PayPal捐助），没钱捧个人场，谢谢各位。

##感激
感谢以下的项目

* [Wind4](https://github.com/Wind4/vlmcsd) 

##关于运行

```javascript
chmod +x vlm*
/root/vlmcsd-armv6hf-Raspberry-glibc
  }
```

##然后随意将代码放入开机启动项rc.local或者哪里定时

##Windows
```javascript
PS C:\WINDOWS\system32> slmgr.vbs -ipk the key from https://technet.microsoft.com/en-us/library/ff793409.aspx or https://technet.microsoft.com/zh-cn/library/jj612867

PS C:\WINDOWS\system32> slmgr.vbs -skms ss.jixu.me

PS C:\WINDOWS\system32> slmgr.vbs -ato

PS C:\WINDOWS\system32> slmgr.vbs -dlv
```
##OFFICE
```javascript
1.Set KMS Host...

x64:

cscript "%ProgramFiles%\Microsoft Office\Office16\ospp.vbs" /sethst:youraddress

x86 installed in Win x64:

cscript "%ProgramFiles(x86)%\Microsoft Office\Office16\ospp.vbs" /sethst:youraddress

2.Request Activation

x64:

cscript "%ProgramFiles%\Microsoft Office\Office16\ospp.vbs" /act

x86 installed in Win x64:

cscript "%ProgramFiles(x86)%\Microsoft Office\Office16\ospp.vbs" /act

3.Clear KMS Host

x64:

cscript "%ProgramFiles%\Microsoft Office\Office16\ospp.vbs" /remhst

x86 installed in Win x64:

cscript "%ProgramFiles(x86)%\Microsoft Office\Office16\ospp.vbs" /remhst

4.Check Activation Status

x64:

cscript "%ProgramFiles%\Microsoft Office\Office16\ospp.vbs" /dstatus

x86 installed in Win x64:

cscript "%ProgramFiles(x86)%\Microsoft Office\Office16\ospp.vbs" /dstatus
```

##查看到期时间

```javascript
slmgr -xpr
```
