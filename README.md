# WireGuard autosetup for EC2

### Summary 

Set up a Wireguard server automatically on an Amazon Linux 2 instance.

This script will install Wireguard on a server and create an initial interface configuration, then generate user certificates and configurations for each line in the `users.txt` file. It will automatically generate a .conf and append it to the network config for the wg interface and restart the service, as well as generate a .conf for the client & print a QR code.

Client configuration files are generated in the `conf/` dir and QR codes are saved in `qr/`.

### Instructions

Clone repo and run `install`. This will automatically generate an installation and create initial users.

Manually create new users with `/etc/wireguard/new`, passing the username as a parameter (e.g. `./new reid`). 

All generated user configurations will be in `/etc/wireguard/conf`
