# pikms
arm kms go go go

pi3 just choose 
and run vlmcsd-armv7el-uclibc-static in command line

pi B 
can run both vlmcsd-armv4el-uclibc-static or vlmcsd-armv5el-musl-thumb-static

if need start at boot just found the 

rc.local this file add the full location of 

where you put like 
/root/vlmcsd-armv7el-uclibc-static 

before

exit 0 

Then Save it will ok


run chmod +x /vlm* at end but do it at first after wget the files you need !!!

Other Linux use command lscpu check the deatail of the CPU the choose the right file


Windows System
PS C:\WINDOWS\system32> slmgr.vbs -upk

PS C:\WINDOWS\system32> slmgr.vbs -ipk  the key from https://technet.microsoft.com/en-us/library/ff793409.aspx

PS C:\WINDOWS\system32> slmgr.vbs -skms ss.jixu.me

PS C:\WINDOWS\system32> slmgr.vbs -ato

PS C:\WINDOWS\system32> slmgr.vbs -dlv



Windows Office：

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

