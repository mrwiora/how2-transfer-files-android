```
- enable developer mode on your mobile phone
- enable usb debugging on developer settings
- execute - adb shell - allow on device by acknowledging fingerprint
- optinoal: execute once more - you should get a shell
- find path like
sunfish:/storage/self/primary/DCIM $ ls -la
total 92
drwxrwx--- 2 root everybody 118784 2021-02-12 18:26 Camera
- copy files directly
adb pull /storage/self/primary/DCIM/Camera

in case you experience connection resets via usb - transfer files via network - e.g. with WSL:
# adb for linux wget https://dl.google.com/android/repository/platform-tools-latest-linux.zip
- start tcpip stack via usb
adb tcpip 5555
- copy files via network
~/platform-tools/adb -s {{ip of mobile device}}:5555 pull /storage/self/primary/WhatsApp/
```
