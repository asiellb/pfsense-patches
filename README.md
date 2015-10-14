# pfsense-patches
Pfsense patches
## Creating patches
login as root user on pfsense appliance

copy original template file

`cp /etc/inc/services.inc /etc/inc/services.inc.org`

edit /etc/inc/services.inc and test changes

create patch
`diff -u /etc/inc/services.inc.org /etc/inc/services.inc > services.inc.dhcp-innovaphone.patch`

upload patch to this repo
## Applying patches
login as root user on pfsense appliance

download patch from this git repo:

`fetch https://raw.githubusercontent.com/naturalis/pfsense-patches/master/services.inc.dhcp-innovaphone.patch`

patch template:

`patch /etc/inc/services.inc /etc/inc/services.inc.dhcp-innovaphone.patch`

open and save dhcp server configuration in pfsense web interface
