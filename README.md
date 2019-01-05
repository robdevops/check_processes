# check_processes
check_processes plugin for Nagios / Icinga. Checks whether all the specified processes are running.

## Description   

## Dependencies
* procps
* bash 4.2

## Usage
```
Usage: check_processes [-c 'process1;process2'] [-f 'full command 1;full command 2']
```

### Example output
```
check_processes -c 'httpd;crond;ntpd' -f 'node server.js start;node client.js start;php collect;php listen'
OK: 7 of 7 processes found: httpd, crond, ntpd, node server.js start, node client.js start, php collect; php listen

echo $?
0
```

```
/usr/local/bin/check_processes -c 'httpd;crond;ntpd;mysqld;master'
CRITICAL: 1 missing process(es): master.

echo $?
2
```
