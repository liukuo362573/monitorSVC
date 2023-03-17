# monitorSVC for arm32
> Used to monitor svc calls of running android apps

## Compile
```
SET PATH=%PATH%;D:\ProgramFiles\Android\Sdk\ndk\21.1.6352462\toolchains\llvm\prebuilt\windows-x86_64\bin
clang -target armv7a-linux-androideabi21 attach.c -o monitorSVC
```

## Usage
```
adb push monitorSVC /data/local/tmp
adb shell chmod 777 /data/local/tmp/monitorSVC

adb shell
./data/local/tmp/monitorSVC  -p $pid <pid to be traced>
	[-L] <list sysCallTable>
	[-v sysCallNo]* <ignore sysCallNo>
	[-e sysCallNo]* <filter sysCallNo>
```

## Demo
<img decoding="async" src="https://raw.githubusercontent.com/liukuo362573/monitorSVC/master/monitorSVC.png" width="30%">
    