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
