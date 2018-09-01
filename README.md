# check_processes
check_processes plugin for Nagios / Icinga. Checks whether all the specified processes are running.

## Description   

## Dependencies
* procps
* bash

## Usage
```
Usage: check_processes <process list>
```

### Example output
```
/usr/local/bin/check_processes httpd crond ntpd mysqld
OK: 4 of 4 processes found: httpd crond ntpd mysqld.

echo $?
0
```

```
/usr/local/bin/check_processes httpd crond ntpd mysqld master
CRITICAL: 1 missing process(es): master.

echo $?
2
```
