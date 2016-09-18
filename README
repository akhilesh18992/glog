# Configurable [glog]

This is forked from [glog].
glog is a leveled logging package for golang which is not much configurable. Motivation for this fork was to make flushinterval, logfile name configurable.

Default behaviour:

- log flush interval 30s
- logfile name program.host.userName.tag.Year.Month.Day.Hour.Minute.Second.pid

Install

```go get https://github.com/akhilesh18992/glog```

Usage

Lets Start with existing features glog features
```
bin/program -v=2 -log_dir=./logs/
```
Loglevel set at 2, log directory as logs. Logs flush at interval of 30 sec
logfile name: program.hostname.username.log.ERROR.20160918-202442.46452

Added flags
```
bin/program -v=2 -log_dir=./logs/ -infologfilename=program.INFO.log -errorlogfilename=program.ERROR.log -warninglogfilename=program.WARNING.log flushinterval=1
```
Logs flush at every 1 sec(helpful during development) and logfile name: program.INFO.log(a bit more readable)
You can also set the flags with same logfile name.
Note: flusinterval flag doesn't start with a hyphen and must be placed at the end otherwise any flag after it would be rejected.

[glog]: <https://github.com/golang/glog>
