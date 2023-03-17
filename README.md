# monitorSVC for arm32
> Used to monitor svc calls of running android apps

## Usage

adb push monitorSVC /data/local/tmp
adb shell chmod 777 /data/local/tmp/monitorSVC

./data/local/tmp/monitorSVC  -p $pid <pid to be traced>
	[-L] <list sysCallTable>
	[-v sysCallNo]* <ignore sysCallNo>
	[-e sysCallNo]* <filter sysCallNo>
    