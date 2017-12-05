# ansible-unattended-upgrades

Sets up unattended upgrades on systems to make sure they stay up to date.

[![Licence](https://img.shields.io/badge/Licence-MIT-blue.svg)](https://opensource.org/licenses/MIT)
[![Platforms](http://img.shields.io/badge/platforms-ubuntu-lightgrey.svg?style=flat)](#)

Tunables
--------
* `unattended_upgrades_package_blacklist` (enumerated list) - (updates|proposed|backports) Automatically upgrade packages from these (origin:archive) pairs can have the values (Please note security updates and Extended Security Maintenance (ESM) are hard coded in the configuration file)
* `unattended_upgrades_allowed_origins` (list) - List of packages to not update
* `unattended_upgrades_update_package_lists` (integer) - "apt-get update" automatically every n-days (0=disable)
* `unattended_upgrades_autoclean_interval` (integer) - "apt-get autoclean" every n-days (0=disable)
* `unattended_upgrades_unattended_upgrade` (integer) - "unattended-upgrade" security upgrade script every n-days (0=disabled)

Example Playbook
----------------
    - hosts: servers
      roles:
         - role: telusdigital.unattended-upgrades


Contributors
------------
* Steven Harradine
