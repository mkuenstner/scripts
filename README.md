scripts
=======

helper/tool scripts

apache-statsd
-------------
Push some apache request metrics directly to statsd, without using any additional tools or log parser.

Add the following lines to any vhost configuration:
```
LogFormat "bytes:%B|msec:%D|method:%m|status:%s|requests:1" apache-statsd-log
CustomLog "|/path/to/apache-statsd appname" apache-statsd-log
```