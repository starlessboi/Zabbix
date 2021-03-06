if.speed
========

This script quey the speed of an interface using the ifSpeed and ifHighSpeed OID and return the right speed value for an interface.

Installation
------------

1. Install `if.speed` in the **ExternalScripts** directory of your Zabbix server and/or proxy. Check your `zabbix_server.conf` and/or `zabbix_proxy.conf` if in doubt.
2. Then chmod a+x `if.speed`
3. Install SNMP gem `gem install snmp`

### Requirements

This script was tested for Zabbix 2.0.0 or higher.

###### [Ruby](http://www.ruby-lang.org/en/downloads/) 1.8.7

This script require Ruby 1.8.7 or higher.

###### [RubyGems](http://rubygems.org) 1.8

This script require RubyGems 1.8 or higher.

###### [SNMP](http://rubygems.org/gems/snmp) 1.1.0

This script require SNMP gem 1.1.0 or higher.

Usage
-----

### As a script
    ./if.speed [OPTIONS]

    where OPTIONS are :
     -h, --help                       Display this help message
     -d, --device IP_ADDRESS          Device IP address discovered by Zabbix
     -c, --community SNMP_COMMUNITY   SNMP community used for the device
     -s, --snmpindex SNMP_INDEX       SNMP index

### As an item
Use `if.speed` like an **External Check** item in Zabbix. So, when creating an item, select **External Check**.  In the **Key** field, you specify:

    if.speed["-d","IP_ADDRESS","-c","SNMP_COMMUNITY","-s","SNMPINDEX"]

Version
-------

Version 1.0

License
-------

This scriptis distributed under the terms of the GNU General Public License as published by the Free Software Foundation; either version 2 of the License, or (at your option) any later version.

### Copyright

  Copyright (c) 2012 Jean-Jacques Martrès

### Authors

  Jean-Jacques Martrès
  (jjmartres |at| gmail |dot| com)
