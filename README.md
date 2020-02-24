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


##如果运行的是 vlmcsdmulti-armv6hf-Raspberry-glibc
```javascript
vlmcsd 1112, built 2018-10-20 09:49:34 UTC

Usage:
   vlmcsd [ options ]

Where:
  -u <user>             set uid to <user>
  -g <group>            set gid to <group>
  -a <csvlk>=<epid>     use <epid> for <csvlk>
  -r 0|1|2              set ePID randomization level (default 1)
  -C <LCID>             use fixed <LCID> in random ePIDs
  -H <build>            use fixed <build> number in random ePIDs
  -o 0|1|2|3            set protection level against clients with public IP addr                esses (default 0)
  -x <level>            exit if warning <level> reached (default 0)
  -L <address>[:<port>] listen on IP address <address> with optional <port>
  -P <port>             set TCP port <port> for subsequent -L statements (defaul                t 1688)
  -F0, -F1              disable/enable binding to foreign IP addresses
  -m <clients>          Handle max. <clients> simultaneously (default no limit)
  -e                    log to stdout
  -D                    run in foreground
  -K 0|1|2|3            set white-listing level for KMS IDs (default -K0)
  -c0, -c1              disable/enable client time checking (default -c0)
  -M0, -M1              disable/enable maintaining clients (default -M0)
  -E0, -E1              disable/enable start with empty client list (default -E0                , ignored if -M0)
  -t <seconds>          disconnect clients after <seconds> of inactivity (defaul                t 30)
  -d                    disconnect clients after each request
  -k                    don't disconnect clients after each request (default)
  -N0, -N1              disable/enable NDR64
  -B0, -B1              disable/enable bind time feature negotiation
  -p <file>             write pid to <file>
  -i <file>             use config file <file>
  -j <file>             use KMS data file <file>
  -R <interval>         renew activation every <interval> (default 1w)
  -A <interval>         retry activation every <interval> (default 2h)
  -l syslog             log to syslog
  -l <file>             log to <file>
  -T0, -T1              disable/enable logging with time and date (default -T1)
  -v                    log verbose
  -q                    don't log verbose (default)
  -V                    display version information and exit

```

```javascript
vlmcs 1112, built 2018-10-20 09:49:34 UTC

Usage: vlmcs [options] [ <host>[:<port>] | .<domain> | - ] [options]

Options:

  -v Be verbose
  -l <app>
  -4 Force V4 protocol
  -5 Force V5 protocol
  -6 Force V6 protocol
  -i <IpVersion> Use IP protocol (4 or 6)
  -j <file> Load external KMS data file <file>
  -e Show some valid examples
  -x Show valid Apps
  -d no DNS names, use Netbios names (no effect if -w is used)
  -V show version information and exit

Advanced options:

  -a <AppGUID> Use custom Application GUID
  -s <ActGUID> Use custom Activation Configuration GUID
  -k <KmsGUID> Use custom KMS GUID
  -c <ClientGUID> Use custom Client GUID. Default: Use random
  -o <PreviousClientGUID> Use custom Prevoius Client GUID. Default: ZeroGUID
  -K <ProtocolVersion> Use a specific (possibly invalid) protocol version
  -w <Workstation> Use custom workstation name. Default: Use random
  -r <RequiredClientCount> Fake required clients
  -n <Requests> Fixed # of requests (Default: Enough to charge)
  -m Pretend to be a virtual machine
  -G <file> Get ePID/HwId data and write to <file>. Can't be used with -l, -4, -5, -6, -a, -s, -k, -r and -n
  -T Use a new TCP connection for each request.
  -N <0|1> disable or enable NDR64. Default: 1
  -B <0|1> disable or enable RPC bind time feature negotiation. Default: 1
  -t <LicenseStatus> Use specfic license status (0 <= T <= 6)
  -g <BindingExpiration> Use a specfic binding expiration time in minutes. Default 43200
  -P Ignore priority and weight in DNS SRV records
  -p Don't use multiplexed RPC bind

<port>:         TCP port name of the KMS to use. Default 1688.
<host>:         host name of the KMS to use. Default 127.0.0.1
.<domain>:      find KMS server in <domain> via DNS
<app>:          (Type vlmcs -x to see a list of valid apps)

```

