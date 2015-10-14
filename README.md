# pfsense-patches
Pfsense patches
## Creating patches
login as root user on pfsense appliance

cp /etc/inc/services.inc /etc/inc/services.inc.org

edit /etc/inc/services.inc and test changes

diff -u /etc/inc/services.inc.org /etc/inc/services.inc > services.inc.dhcp-innovaphone.patch

upload patch to this repo
## Applying patches
login as root user on pfsense appliance

download patch from this git repo

patch /etc/inc/services.inc /etc/inc/services.inc.dhcp-innovaphone.patch

open and save dhcp server configuration in pfsense web interface
