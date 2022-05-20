1.Qu'est-ce que c'est qu'APACHE2
    Apache2 est un serveur HTTP, c'est à dire un module chargé de recevoir et de renvoyer des données selon le protocole HTTP. En d'autres terme, le navigateur internet de l'internaute envois des requêtes à apache2 et en retour apache2 renvoie les données des pages à afficher du site internet que l'internaute est en train de consulter.
    
2.Installation de APACHE2 sur linux
    Pour l'installation d'apache2 , on utilise la commande : apt-get install apache2
    uis on redemarre le système par /etc/init.d/apache2 restart

3.Configuration d'APACHE2 dans le système
    le fichier de configuration d'apache2 se trouve dans : /etc/apache2/apache2.conf 
    puis pour savoir si le serveur est bien installer , il faut taper la commande "/etc/init.d/apavhe2 status

4.Créez un fichier à
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

5.Créez un répertoire pour le site Web, puis créez index.htmlun fichier pour le site Web.
    $ mkdir /var/www/yourdomain.com

    Web, puis créez index.html un fichier pour le site Web.
    $ vi /var/www/yourdomain.com/index.html

   puis redémarrez encore une fois le service Apache pour que les modifications ci-dessus prennent effet avec :
                $ sudo systemctl restart apache2

    *Ouvrez n'importe quel navigateur et entrez l'URL du site Web.
    ==> http://yourdomain.com

Félicitations !... Vous avez réussi à installer APACHE 👏
