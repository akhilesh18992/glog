# Configurable [glog]

This is forked from [glog].
glog is a leveled logging package for golang which is not much configurable. Motivation for this fork was to make flushinterval, logfile name configurable.


## Default behaviour:

- Log flush interval 30s
- Log file name: program.host.userName.tag.Year.Month.Day.Hour.Minute.Second.pid


## Install

```
go get github.com/akhilesh18992/glog
```


## Usage

Lets Start with existing glog features

```
bin/program -v=2 -log_dir=./logs/
```

Loglevel: 2

Log directory: logs

Logs flush interval: 30 sec 

Log file name: program.hostname.username.log.ERROR.20160918-202442.46452


## Added flags

```
bin/program -v=2 -log_dir=./logs/ -infologfilename=program.INFO.log -errorlogfilename=program.ERROR.log -warninglogfilename=program.WARNING.log flushinterval=2
```

Logs flush interval: 2 sec(helpful during development)

Log file name: program.INFO.log(a bit more readable)


You can also set the flags with same logfile name.

```
bin/program -v=2 -log_dir=./logs/ -infologfilename=program.log -errorlogfilename=program.log -warninglogfilename=program.log flushinterval=2
```

Log file name: program.log(All logs/errors/warning are written in same file)

Note: flushinterval flag doesn't start with a hyphen and must be placed at the end otherwise any flag after it would be rejected.


[glog]: <https://github.com/golang/glog>
