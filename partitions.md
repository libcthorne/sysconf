# Partition sizes

A record of partition sizes I've tried using.

## Attempt 2

* 6GB swap space, logical
* 40GB /, logical
* 60GB /home, logical

## Attempt 1

Ubuntu 15.04 (after one year of usage)

* 6.52GiB swap space; seemingly fine; *linux-swap*
* 67.99GiB extended partition
  * 28.39GiB system space; just over 50% used; *ext4*
  * 39.59GiB for /home; 90% used, **too small**; *ext4*

Windows 7 (after one year of usage)

* 100MiB system reserved; seemingly fine (automatically allocated)
* 38.96GiB system+home space; 90% used, **slightly too small**
