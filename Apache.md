#Version 2.4
#Autoriser l’accès depuis une adresse IP avec « Require ip »
  <Directory "/var/www/perso">
     Require all denied
     Require ip 14.14.14.14 50.50.50.50
  </Directory>
#Autoriser l’accès depuis une adresse IP avec « Require Host »
  <Directory "/var/www/perso">
     Require all denied 
     Require host mon-serveur-01 ma-machine
  </Directory>

#SSL
##SEC GVM
  SSLProtocol -ALL -TLSv1 -TLSv1.1 -SSLv2 -SSLv3 +TLSv1.2 +TLSv1.3
  SSLHonorCipherOrder On
  SSLCipherSuite HIGH:!aNULL:!MD5
  SSLCompression off
