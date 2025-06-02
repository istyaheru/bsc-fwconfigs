# bsc-fwconfigs
 Firewall configuration files as mentioned in Eriks Lijurovs' bachelor's degree thesis "Testing and Comparison of the Latest Firewalls for Workstations and Servers"

## To use the templates
The files published here are usable on the default firewalls of the OSs the folders are named after. So files from the ubuntu folder can be used on both Ubuntu Desktop and Ubuntu Server, just as long as the running firewall is ufw. The instructions below are from the point of download.
### Ubuntu template
To apply this template, once you've downloaded the files, copy them over to the `/etc/ufw` directory either graphically (this is unlikely to work as the file manager doesn't have sudo rights) or with the command `sudo cp before.rules before6.rules /etc/ufw`. To apply them, use `sudo ufw reload`, but be mindful that **ufw lets everything through while reloading**

### Fedora template
To apply this template, once you've downloaded the files, copy them over to the `/etc/firewalld/zones` directory with `sudo cp CustomPublic.xml /etc/firewalld/zones`, then reload firewalld to make the zone enablable. To enable it, run `sudo firewall-cmd --set-default-zone=CustomPublic`.

### Windows 11 template
To apply this template, once you've downloaded the files, go to Settings -> Privacy and Security -> Windows Security -> Firewall & Network Protection -> Advanced Settings _(Click Yes when prompted)_ -> Action -> Import Policy _(Click Yes when prompted)_ -> Select the .wfw template file -> Open -> OK.
