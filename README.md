# bemanager

FreeBSD utility to manage, backup, and restore Boot Environments on ZFS filesystems from an easy to use Text User Interface(TUI), bemanager is actually a wrapper around the well known FreeBSD [beadm](https://www.freebsd.org/cgi/man.cgi?query=beadm) and [bectl](https://www.freebsd.org/cgi/man.cgi?query=bectl) utilities.

The utility also uses the default zfs send/receive commands for BootEnvironment@Snapshot backup and restoration to/from either local or remote storage with either XZ or GZIP compression or RAW images.

Please note that this utility is not intended to be a replacement for the previously mentioned utilities, but rather for the ease of some common task on demand.


## Installation

For now there is no installer yet, but you can simply copy and paste the single line command below on ssh for installation:

```
fetch --no-verify-peer https://github.com/JRGTH/bemanager/archive/master.zip && tar -xvf master.zip --strip-components 1 'bemanager-master/bemanager*' && chmod 555 bemanager && mv bemanager /usr/local/sbin/ && mv bemanager.conf.sample /usr/local/etc/ && rm master.zip
```

## Screenshots

![Bemanager Menu TUI](/docs/images/Bemanager_Menu_TUI.png)
![Bemanager Bootenv Backup](/docs/images/Bemanager_Bootenv_Backup.png)
![Bemanager Bootenv Restore](/docs/images/Bemanager_Bootenv_Restore.png)


## CLI Options

```
# bemanager -h
Usage: bemanager [option] [beName | beName@snap | fileName] | [local | remote]
Options:
      -a | --activate  Activate Boot Environment.
      -c | --create    Create Boot Environment.
      -m | --mount     Mount Boot Environment.
      -u | --umount    Unmount Boot Environment.
      -n | --rename    Rename Boot Environment.
      -b | --backup    Backup Boot Environment.
      -r | --restore   Restore Boot Environment.
      -s | --snapshot  Snapshot Boot Environment.
      -d | --destroy   Destroy Boot Environment.
      -v | --version   Display version and exit.
      -h | --help      Display this help message.
#
```

## Notice:
As for version `0.8.0` the configuration has changed and is no longer compatible with previous `bemanager` versions, please check the `bemanager.conf.sample` after upgrade then update current `bemanager.conf` accordingly.
