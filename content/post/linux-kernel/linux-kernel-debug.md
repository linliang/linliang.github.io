---
title: "Linux Kernel Debugging"
date: 2021-05-30T21:20:50+08:00
draft: false
---

#### Trace max stack

``` bash
mount -t de bugfs nodev /sys/kernel/debug
cat /proc/sys/kernel/stack_tracer_enabled
echo 1 > /proc/sys/kernel/stack_tracer_enabled
cat /sys/kernel/debug/tracing/stack_max_size -> 紀錄stack最大時多少
watch
cat /sys/kernel/debug/tracing/stack_trace -> 對應的call stack trace
```
