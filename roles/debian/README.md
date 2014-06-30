ansible-debian_up2date
======================

Ansible role to keep a Debian installation up to date.

By default, it does the following:

- Add the 'testing' repositories
- Set 'stable' as the default release
- Do a safe upgrade to the latest (stable) version
- Install and configure unattended-upgrades
