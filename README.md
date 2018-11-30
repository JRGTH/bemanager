# bemanager

FreeBSD utility to manage, backup, and restore Boot Environments on ZFS filesystems from an easy to use Text User Interface(TUI), bemanager is actually a wrapper around the well known FreeBSD beadm utility.

The utility also uses the default zfs send/receive commands for BE/Snap backup and restoration to/from either local or remote storage with XZ compression but is not limited to.

Please note that I'm not a programmer by trade, also this utility is not intended to be a replacement for the command line, but for the ease of some common task on demand.


## Installation

For now there is no installer yet, but you can simply copy and paste the single line below command on ssh for installation:

```
fetch --no-verify-peer https://github.com/JRGTH/bemanager/archive/master.zip && tar -xf master.zip --strip-components 1 bemanager-master/bemanager && chmod 555 bemanager && mv bemanager /usr/local/sbin/bemanager && rm master.zip; rehash
```

## Screenshot

![bemanager](https://drive.google.com/uc?export=download&id=14X0jSTBXJbdeUQznB5-l7jRLyKGrNQ3B)
