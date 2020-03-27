# Linux_Server_Configuration
Udacity Full Stack Development Nano Degree Final Project

### Owner
Ibraheem Alyan

### Overview
This repositary is only a guide to access the configured linux server on Amazon LightSale

## Info

### SSHing into the server

- Public IP : 3.124.200.75
- SSH port : 2200
- User : grader
- Private RSA Key File : private_key.rsa
- Key Pair Passphrase : Grader@098

* note that SSHing via passwords is unpermitted ( only RSA key-based SSH authentication is allowed )

### root access
The user "grader" is given root privilges
- grader's Password : !23@Grader

### Item Catalog
you can visit the item catalog web app that is hosted on the seever via 
-     https://3.124.200.75.xip.io/
* you may get a warning ⚠️ because of invalid ssl certification just click advanced and skip it

## How I configured the server

* added the grader user 
* set root access for user grader
* installed postegresql and apache http server
* setup the database through a python script 
* connected the flask app to the apache server throug mod-wsgi
* setup self signed SSL certification 
* configured ssh keys for each user and disallowed ssh via passwords
* changed ssh port to a non-default port
* configured the ufw to limit unused ports
* DONE

## configuration info

#### webapp directory    
-     /var/www/Item_Catalog

#### wsgi script     
-     /var/www/Item_Catalog/my_app.wsgi

#### error log    
-     /var/log/apache2/error.log

* apache2 site configuration files
-     /etc/apache2/sites-available/000-default.conf
-     /etc/apache2/sites-available/default-ssl.conf

#### postegresql user    
-     postgres

#### SSL certificate and key       
-     /etc/ssl/private/apache-selfsigned.key
-     /etc/ssl/certs/apache-selfsigned.crt
 
#### flask webapp output log      
-     /home/ubuntu/output.log
