---
title: Disk utilization
brief: Percent of disk used on this volume. 
metric_type: gauge
---
### Disk utilization

This metric shows the amount of disk space in use on this volume, as a percentage of total disk space available on the volume. The SignalFx metadata plugin computes this metric based on the disk space metrics output by the `disk` plugin for telegraf, as follows:

```
100 * [disk.used / (disk.free + disk.used)] 
```
