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

Link MacPorts to the repository.

Open /opt/local/etc/macports/sources.conf file in a text editor. Insert a
URL pointing to the reposity location before the rsync URL as shown.

```
file:///opt/local/var/shared/sources/ports
rsync://rsync.macports.org/release/ports [default]
```

Update the MacPorts index.

After you create or the repository, use the MacPorts
portindex command to create or update the index of the ports.

```bash
$ cd /opt/local/var/shared/sources/Ports
$ sudo portindex
```

Apply future updates.

```bash
$ cd /opt/local/var/shared/sources/Ports
$ sudo git pull https://github.com/brianspeir/Ports.git
sudo portindex
```

###Available Ports

####Ansible 1.3.2

Ansible is a radically simple IT orchestration engine that makes your applications and systems easier to deploy. Avoid writing scripts or custom code to deploy and update your applications— automate in a language that approaches plain English, using SSH, with no agents to install on remote systems. http://www.ansibleworks.com
