## shutdown_if_battery_low

<!-- This file was generated by Ansigenome. Do not edit this file directly but
     instead have a look at the files in the ./meta/ directory. -->

[![Ansible Galaxy](http://img.shields.io/badge/galaxy-ypid.shutdown_if_battery_low-660198.svg?style=flat)](https://galaxy.ansible.com/detail#/role/3778)
[![Platforms](http://img.shields.io/badge/platforms-debian-lightgrey.svg?style=flat)](https://galaxy.ansible.com/detail#/role/3778)
[![GitHub Tags](https://img.shields.io/github/tag/ypid/ansible-shutdown_if_battery_low.svg)](https://github.com/ypid/ansible-shutdown_if_battery_low)
[![GitHub Stars](https://img.shields.io/github/stars/ypid/ansible-shutdown_if_battery_low.svg)](https://github.com/ypid/ansible-shutdown_if_battery_low)


Shutdown the system if the build-in battery is low.

Based on blogpost [Debian - Convert a EEE 701 as a server with embeded UPS](http://bernaerts.dyndns.org/linux/75-debian/200-debian-eeeserver-powerfailure).

### Installation

This role requires at least Ansible `v2.1.3`. To install it, run:

```Shell
ansible-galaxy install ypid.shutdown_if_battery_low
```

To install via git, run either:

```Shell
git clone https://github.com/ypid/ansible-shutdown_if_battery_low.git ypid.shutdown_if_battery_low
git submodule add https://github.com/ypid/ansible-shutdown_if_battery_low.git ypid.shutdown_if_battery_low
```



### Role variables

List of default variables available in the inventory:

```YAML
---

## When the battery capacity in percent is less then the following value,
## write a log entry check interval (refer to ``shutdown_if_battery_low__sleep``).
shutdown_if_battery_low__limit_warn: 60

## When the battery capacity in percent is less then the following value, the
## system is going to shutdown.
shutdown_if_battery_low__limit_shutdown: 20

## Command to execute when battery capacity in percent <= shutdown_if_battery_low__limit_shutdown
shutdown_if_battery_low__shutdown_command: 'shutdown --poweroff +5'

## Check interval/sleep time between check.
shutdown_if_battery_low__sleep: '6m'

shutdown_if_battery_low__script_filepath: "/usr/local/bin/shutdown_if_battery_low.sh"
shutdown_if_battery_low__environment_filepath: "/etc/default/shutdown_if_battery_low"
```




### Authors and license

`shutdown_if_battery_low` role was written by:

- [Robin Schneider](http://ypid.de/) | [e-mail](mailto:ypid@riseup.net) | [Twitter](https://twitter.com/ypid) | [GitHub](https://github.com/ypid)

License: [AGPLv3](https://tldrlegal.com/license/gnu-affero-general-public-license-v3-%28agpl-3.0%29)

***

README generated by [Ansigenome](https://github.com/nickjj/ansigenome/).
