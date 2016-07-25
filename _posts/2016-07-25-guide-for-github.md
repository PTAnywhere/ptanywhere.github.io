---
layout: post
title:  "Understanding Github projects"
date:   2016-07-25 15:42:00
categories: main
---

This article describes the projects under the
[PT Anywhere organization](https://github.com/PTAnywhere).
These projects can be divided in the following categories:

*   Installation scripts
*   The core projects
*   Related secondary projects

## Installation scripts

*   __[PA-installation](https://github.com/PTAnywhere/ptAnywhere-installation)__:
contains scripts which ease the installation and deployment of all its
components.

## Core projects

_PT Anywhere_ (PA)  __front-end__ projects:

*   __[PA-widget](https://github.com/PTAnywhere/ptAnywhere-widget)__:
    [Angular JS](https://angularjs.org/) application to create PA widgets.

*   __[PA-frontend](https://github.com/PTAnywhere/ptAnywhere-widget)__:
    Java ([Jersey](https://jersey.java.net/)) web application which serves
    _PA-widget_.

*   (deprecated) ~~__[PA-js](https://github.com/PTAnywhere/ptAnywhere-js)__:
    [jQuery-based](https://jquery.com/) HTTP library for the API.~~

PA __back-end__ projects:

*   __[PA-api](https://github.com/PTAnywhere/ptAnywhere-api)__:
    An HTTP API for Packet Tracer made in Java (Jersey).

*   __[pt-instances-management](https://github.com/PTAnywhere/pt-instances-management)__:
    An internal HTTP API for creating and managing different instances of
    _Packet Tracer_.
    It is Python application which uses [Flask](http://flask.pocoo.org/) and
    [Celery](http://celery.readthedocs.io).
    Instances run in [Docker](https://www.docker.com/) containers.

*   __[PTChecker](https://github.com/PTAnywhere/pt-checker)__ hosts both
    a Python and a Java library to check if a _Packet Tracer_ instance is
    running on a given host and port.
    This application is used by _pt-instances-management_ to monitor
    _Packet Tracer_ instances.

## Secondary projects

Additionally, we have also made public the following related projects:

*   __[performance-testing](http://ptanywhere.github.io/performance-testing/)__:
    a Python project created to measure the performance of _PT Anywhere_
    (specifically the Docker-based _Packet Tracer_ container).

*   __[usage-analysis](https://github.com/PTAnywhere/usage-analysis)__:
    a web application which visualizes users interactions with the widgets in
    different ways.
