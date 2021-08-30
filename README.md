# wmic
originally taken from wmi-1.3.14 from openvas?

pretty much replaced with https://edcint.co.nz/checkwmiplus/download/wmic-source-v1-4-1/ which is modified from zenoss

This works against windows 20H1

I tweaked the GNUmakefile to include `-ffreestanding` to help with newer GCCs

run make with sudo because it will immediately install into `/bin/wmic` and `/bin/winexe`

shows as version 1.4.1

Common issues
---
too many files open

probably `ulimit -Sn` is too small
open it up a little by editing `/etc/security/limits.conf` and adding something like
```
bob    soft nofile 4096
```