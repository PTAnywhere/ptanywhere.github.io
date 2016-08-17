---
layout: post
title:  "Troubleshooting"
category: general
---

Some of these problems might be open issues pending to be fixed.

## Packet Tracer Manager's API shows a 502 error

__Description__: nginx returns a _502 Bad Gateway_ error.

__Solution__ execute and wait some seconds:

{% highlight shell %}
sudo supervisorctl restart flask_app
{% endhighlight %}


## Installation

### Missing password in Ansible

Ansible throws an error which says: ```Missing become password```.

 * What happens? The remote user you are running needs to introduce a password to become sudo.
 * Quick solution: Add the ```--ask-become-pass``` parameter.

### Docker image building

The Docker image cannot been built correctly the first time you run the Ansible script: ```dial unix /var/run/docker.sock: permission denied ```

 * What happens? The SSH connection used by Ansible does not know that the user is now part of the _docker_ group (because it has join the group within the same session). This problem is explained in more detail [here](http://stackoverflow.com/questions/26677064/create-and-use-group-without-restart) (BTW, the solution described there does not work for me).
 * Quick solution: run the Ansible script (or the Vagrant one which uses it) a second time.

### Packet Tracer gets stuck because of an HTTP proxy

The PT instance gets stuck in a machine running behind a HTTP proxy and logs don't show any meaningful information.

 * Strange as it may sound, you might want to [unset the proxy for PacketTracer](https://github.com/PTAnywhere/ptAnywhere-installation/commit/b7518b994264c0516e540e21261e96cf6bc77318).
