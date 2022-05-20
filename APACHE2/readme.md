1.Qu'est-ce que c'est qu'APACHE2
    Apache2 est un serveur HTTP, c'est à dire un module chargé de recevoir et de renvoyer des données selon le protocole HTTP. En d'autres terme, le navigateur internet de l'internaute envois des requêtes à apache2 et en retour apache2 renvoie les données des pages à afficher du site internet que l'internaute est en train de consulter.
    
2.Installation de APACHE2 sur linux
    Tout d'abord ,il faut vous conneter en tant que 'superutilisateur' avec la commande "su"
    Puis pour l'installation d'apache2 , on utilise la commande : apt-get install apache2
    Après verifier s'il est bien installer avec /etc/init.d/apache2 status
 
3.Configuration d'APACHE2 dans le système
    le fichier de configuration d'apache2 se trouve dans : /etc/apache2/apache2.conf
    
4.herbergement du site avec apache2
    -D'abord trouver l'adresse IP avec la commande " ip addr "
    -puis mettre l'adresse IP dans son navigateur . 
    -Il faut ensuite configurer l'autorisation avec la commande "chmod 755/var/www/html
    -ENTRER  après dans nano /etc/apache2/apache2.conf et rechercher la ligne "Directory":/var/www/ afin de la remplacer par le site de votre choix 
    -Enfin redemarrer le système avec "systemctl restart apache2
    -puis reouvrir dans un navigateur l'url de la page 
    
    
    

Félicitations !... Vous avez réussi à installer APACHE 👏
