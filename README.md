
Description
-------------------------

All original code come from http://sourceforge.net/projects/redmin-mylyncon/

Aim of this fork is to provide git mirror of above repository as well as place for my own work.
Pull requests will be warm welcomed and served with cold beer ;).

Build status on Travis CI:
[![Build Status](https://travis-ci.org/ljader/redmine-mylyn-plugin.svg)](https://travis-ci.org/ljader/redmine-mylyn-plugin)

Redmine-Mylyn integration
-------------------------

Redmine-Mylyn integration requires 2 components to work:

1. Redmine plugin (connector) - is installed inside Redmine server and publishes an API
2. Eclipse plugin - acts like a client for API from (1) plugin

The Mylyn project in particular has always called the component that adds support for another server a "connector", 
and Redmine usually calls additional components "plugin" - alas, 
the original software project got this the wrong way around and called the server-side component a connector
and the client side component a plugin. Confusion persists unto this day.

Connector Installation
-------------------------

1. Install connectior inside Redmine server
    
    For Redmine 2.x install Connector from:
    [http://danmunn.github.io/redmine_mylyn_connector/](http://danmunn.github.io/redmine_mylyn_connector/)
     
    For Redmine 3.x install Connector from:
    [TODO Link](http://google.com)
     
2. Enable REST API in Redmine server

    This is required, because Eclipse plugin uses REST API to authenticate user and perform requests. 

    To enable REST API go to yours redmine Administration -> Settings -> Authentication tab and toggle on:
    **Enable REST web service** and press **Save**

Plugin Installation
-------------------------

1.  Download latest release from GitHub releases:
[ZIP with built plugin as P2 repo](https://github.com/ljader/redmine-mylyn-plugin/releases/latest)

2.  Install it into Eclipse using instructions from [http://stackoverflow.com/a/16074606/498096](http://stackoverflow.com/a/16074606/498096) section "(1) auto install" - in summary:

		Eclipse Menu -> Help -> Install New Software -> Add -> Archive

		and then choose downloaded .zip file

3. Add Task Repository of type Redmine and provide redmine Url with Login and Password

Development
-------------------------

See the [CONTRIBUTING.md](CONTRIBUTING.md).

Licence
-------------------------
Licence remains as in original plugin, that is:
Eclipse Public License, GNU General Public License (GPL)
