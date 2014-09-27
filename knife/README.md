chef/knife
==========

`debian7-edgeos-raspbian.erb` - knife bootstrap template for debian7-ish
distros to install Chef via ruby gems. In particular I use these for:

* Raspbian for Raspberry Pi
  - Debian 7 'wheezy' for ARM
  - http://www.raspbian.org/

* EdgeOS for Ubiquiti EdgeRouter POE, EdgeRouter Lite
  - Based on Debian 6 'squeeze'
  - Routing stack based on Vyatta fork
  - http://www.ubnt.com/edgemax/edgerouter-lite/

Template based upon
https://github.com/webtatic/configuration/blob/master/chef/bootstrap/debian6-gems.erb
minus databag support.


#### examples

##### Interesting EdgeOS ohai output
```
  "kernel": {
    "machine": "mips64",
    "name": "Linux",
    "os": "GNU/Linux",
    "release": "2.6.32.13-UBNT"
    "version": "#1 SMP Wed Oct 24 01:08:06 PDT 2012",
  },
  "os_version": "2.6.32.13-UBNT",
  "platform": "debian"
  "platform_family": "debian",
  "platform_version": "6.0.6",
```

##### Interesting Raspbian ohai output
```
  "kernel": {
    "machine": "armv6l",
    "name": "Linux",
    "os": "GNU/Linux"
    "release": "3.2.27-pps-g965b922-dirty",
    "version": "#1 PREEMPT Sat Sep 22 16:30:50 EDT 2012",
  },
  "os_version": "3.2.27-pps-g965b922-dirty",
  "platform": "raspbian",
  "platform_version": "wheezy/sid",
  "platform_family": "debian",
```
