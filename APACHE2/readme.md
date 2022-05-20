Créez un fichier à
¢ /etc/apache2/sites-available/yourdomain.com.

*ajoutez-y les lignes suivantes :
$ nano /etc/apache2/sites-available/yourdomain.com.conf

<virtualhost *:80="">

ServerAdmin webmaster@localhost

ServerName yourdomain.com

ServerAlias www.yourdomain.com

DocumentRoot /var/www/yourdomain.com

ErrorLog ${APACHE_LOG_DIR}/error.log

CustomLog ${APACHE_LOG_DIR}/access.log combined

*Créez un répertoire pour le site Web, puis créez index.htmlun fichier pour le site Web.
$ mkdir /var/www/yourdomain.com

*Web, puis créez index.htmlun fichier pour le site Web.
$ vi /var/www/yourdomain.com/index.html

*Redémarrez le service Apache pour que les modifications ci-dessus prennent effet.
$ sudo systemctl restart apache2

*Ouvrez n'importe quel navigateur et entrez l'URL du site Web.
==> http://yourdomain.com

Félicitations !... Vous avez réussi à installer APACHE 👏
