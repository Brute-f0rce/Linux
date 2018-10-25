---
description: >-
  Apparmor will protect the system by confining programs to a limited set of
  resources.
---

# apparmor

## To activate a profile:

sudo aa-enforce usr.bin.firefox

## OR

export _PROFILE_='usr.bin.firefox' sudo $\(rm /etc/apparmor.d/disable/$_PROFILE_ ; cat /etc/apparmor.d/$_PROFILE_ \| apparmor\_parser -a \)

## TO disable a profile:

`sudo aa-disable usr.bin.firefox`

### OR

`export` _`PROFILE`_`='usr.bin.firefox' sudo $(ln -s /etc/apparmor.d/$`_`PROFILE`_ `/etc/apparmor.d/disable/ && apparmor`_`parser -R /etc/apparmor.d/$_PROFILE`_`)`

## To list profiles loaded:

`sudo aa-status`

### OR

`sudo apparmor_status`

## List of profiles aviables: 

`/etc/apparmor.d/`

