ansible-secure
==============

Ansible role for securing a VPS, based on [Bryan Kennedy's blog post](http://plusbryan.com/my-first-5-minutes-on-a-server-or-essential-security-for-linux-servers).

By default, it does the following:

- Install `fail2ban`
- Disable SSH root login
- Disable SSH password authentication
- Install `ufw`
- Selectively allow SSH traffic
- Allow HTTP and HTTPS traffic


Dependencies
------------

This role requires the Ansible `ufw` module, which is not yet part of the standard Ansible distribution. At the
moment, [this PR](https://github.com/ansible/ansible/pull/5518) is the most likely candidate.

Download the file `ufw` and add it to your `modules` directory.

