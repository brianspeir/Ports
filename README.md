Ports
=====

A local MacPorts portfile repository generally providing
Portfiles that are not yet commited or updated to MacPorts.

Create the repository.

```bash
$ sudo mkdir -p /opt/local/var/shared/sources
$ cd /opt/local/var/shared/sources
$ sudo git clone https://github.com/brianspeir/Ports.git
```

Open /opt/local/etc/macports/sources.conf file in a text editor. Insert a
URL pointing to the reposity location before the rsync URL as shown.

```
file:///opt/local/var/shared/sources/ports
rsync://rsync.macports.org/release/ports [default]
```

After you create or update the repository, use the MacPorts
portindex command to create or update the index of the ports.

```bash
$ cd /opt/local/var/shared/sources/Ports
$ sudo portindex
```
