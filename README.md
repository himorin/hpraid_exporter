### hpraid_exporter
Command hpraid_exporter provides a Prometheus exporter for the parsed output of "hpssacli/hpacucli ctrl all show config" command.

### Requirements
By default only root can run hpssacli command, so you need to run exporter from root or permit access to hpssacli executable with sudo

hpssacli should be in $PATH
### Usage

```
$ ./hpraid_exporter --help
Usage of ./hpraid_exporter:
  -cmd string
        command, that shows hpraid stats (default "hpssacli")
  -port string
        port to expose /metrics on (default ":9327")
```

### Comments

This exporter based on https://github.com/gdm85/hpraidmon utility. I just removed some unnecessary(in my opinion) parts and added code that exposes metrics with prometheus client library.
