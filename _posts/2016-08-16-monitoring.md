---
layout: post
title:  "Management and monitoring tools"
category: general
---

A typical _PT Anywhere_ installation can be quite complex because it relies in different components that might be hosted by several machines.

This page lists some of the tools that I find useful to manage and monitor _PT Anywhere_.

## Web client

 * Your favorite web development tool should be enough (e.g., [Firefox developer edition](https://www.mozilla.org/en-US/firefox/developer/)).

## Web server

 * Log files in the [Tomcat log](https://tomcat.apache.org/tomcat-7.0-doc/logging.html) directory.
 * The API is described using [OpenAPI](https://github.com/OAI/OpenAPI-Specification) (formerly known as [Swagger](http://swagger.io/open-source-integrations/)). Therefore, you can use [Swagger-UI](https://github.com/swagger-api/swagger-ui) to explore and test its methods.
 * To debug the web application, [try this](https://github.com/PTAnywhere/ptAnywhere-api/wiki/Debugging).

## Session manager

 * [redis-cli](http://redis.io/topics/quickstart)
 * [This script](https://gist.github.com/gomezgoiri/aafeece829d96fbb13ac) lists current users.

## Packet Tracer manager

 * It exposes an [API](https://github.com/PTAnywhere/pt-instances-management) described using _OpenAPI_. Go to the application root (usually in the port 80) to find a Swagger-UI.
  * [This script](https://gist.github.com/gomezgoiri/fba21334c8f74db4c154) creates N instances in the API.
  * [This script](https://gist.github.com/gomezgoiri/10c7fc1d042ec9dbdee2) deallocates instances and deletes them.
 * The [Docker CLI](https://docs.docker.com/engine/reference/commandline/cli/) can be used to check the containers created and their current status.
  * See some [useful commands here](https://github.com/PTAnywhere/pt-instances-management/wiki)
 * The API internally uses [Celery](http://www.celeryproject.org/). You can use [Flower](http://flower.readthedocs.org/en/latest/) to monitor Celery. Flower should be already installed so start it using ``supervisorctl start celery:flower`` and go to the web application running on __port 5554__ (unless you have changed the default value in the _Ansible_ script).

## Learning Record Store

 * Use the [LearningLocker](http://learninglocker.net/) web dashboard.
 * Use a [client library](https://tincanapi.com/libraries/) to query it.
