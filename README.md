# munin-plugins

These plugins can be used to monitor cpu and memory usage of running docker containers.

Place the docker_ files in the munin plugin directory and restart munin-node.

The user that munin runs as will need permissions to run the docker command as well as access to the cgroups pseudo directories. Update SELinux rules as necessary. Place the following in /etc/munin/plugin-conf.d/munin-node (replace root with whatever user has access that you would like to use):

```[docker_cpu]
user root

[docker_memory]
user root
```
