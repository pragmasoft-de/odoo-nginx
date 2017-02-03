# odoo-nginx
nginx config files for odoo

* for odoo and nginx on the same machine
* replace domain.tld in the nginx config files with the domain of your odoo server
* config is for Let's Encrypt SSL certificates
* replace your openssl.cnf with the one from the repository, otherwise the SSL config in the nginx config files will not work
* create dhparam.pem with `sudo openssl dhparam -out /etc/ssl/certs/dhparam.pem 2048`
