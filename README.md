# OS Linux Pressure Stall Information

## Description

Self-contained template for monitoring pressure stall information on Linux systems. Source: <add tamu git reop here>

## Overview


## Author

Matthew Hielsberg - hielsber@tamu.edu

## Macros used

|Name|Description|Default|Type|
|----|-----------|-------|----|
|{$CPU_FULL_AVG10_THRESH}|CPU starvation for ALL processes over 10 seconds|0|Integer|
|{$CPU_FULL_AVG60_THRESH}|CPU starvation for ALL processes over 60 seconds|0|Integer|
|{$CPU_FULL_AVG300_THRESH}|CPU starvation for ALL processes over 300 seconds|0|Integer|
|{$CPU_SOME_AVG10_THRESH}|CPU starvation for some processes over 10 seconds|75|Integer|
|{$CPU_SOME_AVG60_THRESH}|CPU starvation for some processes over 60 seconds|50|Integer|
|{$CPU_SOME_AVG300_THRESH}|CPU starvation for some processes over 300 seconds|25|Integer|
|{$IO_FULL_AVG10_THRESH}|IO starvation for ALL processes over 10 seconds|10|Integer|
|{$IO_FULL_AVG60_THRESH}|IO starvation for ALL processes over 60 seconds|5|Integer|
|{$IO_FULL_AVG300_THRESH}|IO starvation for ALL processes over 300 seconds|1|Integer|
|{$IO_SOME_AVG10_THRESH}|IO starvation for some processes over 10 seconds|50|Integer|
|{$IO_SOME_AVG60_THRESH}|IO starvation for some processes over 60 seconds|10|Integer|
|{$IO_SOME_AVG300_THRESH}|IO starvation for some processes over 300 seconds|5|Integer|
|{$MEMORY_FULL_AVG10_THRESH}|Memory starvation for ALL processes over 10 seconds|10|Integer|
|{$MEMORY_FULL_AVG60_THRESH}|Memory starvation for ALL processes over 60 seconds|5|Integer|
|{$MEMORY_FULL_AVG300_THRESH}|Memory starvation for ALL processes over 300 seconds|1|Integer|
|{$MEMORY_SOME_AVG10_THRESH}|Memory starvation for some processes over 10 seconds|50|Integer|
|{$MEMORY_SOME_AVG60_THRESH}|Memory starvation for some processes over 60 seconds|10|Integer|
|{$MEMORY_SOME_AVG300_THRESH}|Memory starvation for some processes over 300 seconds|5|Integer|

## Template links

There are no template links in this template.

## Discovery rules

There are no discovery rules in this template

## Items collected

|Name|Description|Type|Key and additional info|
|----|-----------|----|-----------------------|

|CPU Pressure Stall Information - 10s Average|The percentage of stalled tasks on the CPU over the last 10s window.|FLOAT|key: psi_mth.cpu.some.avg10, master_item key: vfs.file.contents[/proc/pressure/cpu]|
|CPU Pressure Stall Information - 60s Average|The percentage of stalled tasks on the CPU over the last 60s window.|FLOAT|key: psi_mth.cpu.some.avg60, master_item key: vfs.file.contents[/proc/pressure/cpu]|
|CPU Pressure Stall Information - 300s Average|The percentage of stalled tasks on the CPU over the last 300s window.|FLOAT|key: psi_mth.cpu.some.avg300, master_item key: vfs.file.contents[/proc/pressure/cpu]|
|IO Pressure Stall Information - Full - 10s Average|The percentage of time all tasks were waiting on IO over the last 10s window.|FLOAT|key: psi_mth.io.full.avg10, master_item key: vfs.file.contents[/proc/pressure/io]|
|IO Pressure Stall Information - Full - 60s Average|The percentage of time all tasks were waiting on IO over the last 60s window.|FLOAT|key: psi_mth.io.full.avg60, master_item key: vfs.file.contents[/proc/pressure/io]|
|IO Pressure Stall Information - Full - 300s Average|The percentage of time all tasks were waiting on IO over the last 300s window.|FLOAT|key: psi_mth.io.full.avg300, master_item key: vfs.file.contents[/proc/pressure/io]|
|IO Pressure Stall Information - Some - 10s Average|The percentage of time some tasks were waiting on IO over the last 10s window.|FLOAT|key: psi_mth.io.some.avg10, master_item key: vfs.file.contents[/proc/pressure/io]|
|IO Pressure Stall Information - Some - 60s Average|The percentage of time some tasks were waiting on IO over the last 60s window.|FLOAT|key: psi_mth.io.some.avg60, master_item key: vfs.file.contents[/proc/pressure/io]|
|IO Pressure Stall Information - Some - 300s Average|The percentage of time some tasks were waiting on IO over the last 300s window.|FLOAT|key: psi_mth.io.some.avg300, master_item key: vfs.file.contents[/proc/pressure/io]|
|Memory Pressure Stall Information - Full - 10s Average|The percentage of time all tasks were waiting on Memory over the last 10s window.|FLOAT|key: psi_mth.memory.full.avg10, master_item key: vfs.file.contents[/proc/pressure/memory]|
|Memory Pressure Stall Information - Full - 60s Average'|The percentage of time all tasks were waiting on Memory over the last 60s window.|FLOAT|key: psi_mth.memory.full.avg60, master_item key: vfs.file.contents[/proc/pressure/memory]|
|Memory Pressure Stall Information - Full - 300s Average|The percentage of time all tasks were waiting on Memory over the last 300s window.|FLOAT|key: psi_mth.memory.full.avg300, master_item key: vfs.file.contents[/proc/pressure/memory]|
|Memory Pressure Stall Information - Some - 10s Average|The percentage of time tasks were waiting on Memory over the last 10s window.|FLOAT|key: psi_mth.memory.some.avg10, master_item key: vfs.file.contents[/proc/pressure/memory]|
|Memory Pressure Stall Information - Some - 60s Average'|The percentage of time tasks were waiting on Memory over the last 60s window.|FLOAT|key: psi_mth.memory.some.avg60, master_item key: vfs.file.contents[/proc/pressure/memory]|
|Memory Pressure Stall Information - Some - 300s Average|The percentage of time tasks were waiting on Memory over the last 300s window.|FLOAT|key: psi_mth.memory.some.avg300, master_item key: vfs.file.contents[/proc/pressure/memory]|
|CPU Pressure Stall Information - Text|Service item for gathering cpu ''some'' pressure (10s,60s,300s)|TEXT|key: vfs.file.contents[/proc/pressure/cpu]|
|IO Pressure Stall Information - Text|Service item for gathering io ''some'' and ''full'' pressure (10s,60s,300s)|TEXT|key: vfs.file.contents[/proc/pressure/io]|
|Memory Pressure Stall Information - Text|Service item for gathering memory ''some'' and ''full'' pressure (10s,60s,300s)|TEXT|key: vfs.file.contents[/proc/pressure/memory]|

## Triggers

There are no triggers in this template.
