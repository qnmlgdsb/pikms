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

CD "%SystemRoot%\SYSTEM32"

CSCRIPT /NOLOGO SLMGR.VBS /SKMS ss.jixu.me

CSCRIPT /NOLOGO SLMGR.VBS /ATO

CSCRIPT /NOLOGO SLMGR.VBS /XPR

Office/Project/Visio 2013(2010 change the location) ：

32bit：CD "%ProgramFiles(x86)%\MICROSOFT OFFICE\OFFICE15"

64bit：CD "%ProgramFiles%\MICROSOFT OFFICE\OFFICE15"

CSCRIPT OSPP.VBS /SETHST:ss.jixu.me

CSCRIPT OSPP.VBS /ACT

CSCRIPT OSPP.VBS /DSTATUS
