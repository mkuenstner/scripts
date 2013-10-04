scripts
=======

helper, tool, scripts

apache-statsd
-------------
Push some apache request metrics directly to statsd, without using any additional tools or log parser.

Add the following lines to any vhost configuration:
```
LogFormat "bytes:%B|msec:%D|method:%m|status:%s|requests:1" apache-statsd-log
CustomLog "|/path/to/apache-statsd appname" apache-statsd-log
```

Custom.css
----------
user stylesheet for modern browser, with some better styling for [xdebug](https://github.com/xdebug/xdebug) errors.

**Chrome**
```
~/Library/Application\ Support/Google/Chrome/Default/User\ StyleSheets/Custom.css
```

github-status
----------
Small shell script to wrap curl call to [github status api](http://developer.github.com/v3/repos/statuses/).

```
github-status -s success -b 231 -o danielMitD -r scripts -c eb66a21c06d85bd327954c1f772a7dc328109912
```
