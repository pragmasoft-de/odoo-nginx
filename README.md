# odoo-nginx
nginx config files for odoo

* for odoo and nginx on the same server
* config works for odoo 8, 9, 10 and 11
* odoo_port_443.site is for SSL/TLS (HTTPS), odoo_port_80.site is for port 80 (HTTP)
* replace odoo.domain.tld in the nginx config files with the external domain name of your odoo server
* SSL config is for Let's Encrypt SSL certificates
* replace your openssl.cnf with the one from the repository in case the SSL config in the nginx config files should not work properly
* create dhparam.pem with `sudo openssl dhparam -out /etc/ssl/certs/dhparam.pem 4096` (may take a couple of minutes to finish)
* copy the appropriate file to /etc/nginx/sites-available and create a symlink to it in /etc/nginx/sites-enabled
* set the parameters `netrpc_interface` and `xmlrpc_interface` in the odoo config file to `127.0.0.1` and restart the odoo service
* check the file with `nginx -t`
* load the new config with `service nginx restart`
