### Mac command line notes


networksetup -listallhardwareports
networksetup -setsecurewebproxy wi-fi 192.168.86.36 3128
networksetup -setwebproxystate "USB 10/100/1000 LAN" on
networksetup -setwebproxystate "USB 10/100/1000 LAN" off


**check USB**
```bash 
ioreg -p IOUSB -w0 | sed 's/[^o]*o //; s/@.*$//' | grep -v '^Root.*'
```
or
```bash
system_profiler SPUSBDataType
```


LaunchAgents
```bash
defaults read com.apple.dock.plist|grep "file:"| cut -d\" -f4 | cut -d. -f1| cut -d\/ -f5

```
