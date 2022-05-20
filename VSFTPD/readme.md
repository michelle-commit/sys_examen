1.DESCRIPTION (vsftpd)
    VsFTPd est un serveur FTP conçu avec la problématique d'une sécurité maximale. Contrairement aux autres serveurs FTP (ProFTPd, PureFTPd, etc.), aucune faille majeure de sécurité n'a jamais été décelée dans VsFTPd.
    
2.INSTALLATION
        Ici, on va voir l'installation d'un serveur vsftpd et montrer comment connecter un client à ce partage.
        Tout d'abord mettons à jour notre systeme avec "apt udate "

        Puis , l'installation se poursuit par :$ sudo apt install vsftpd 
        NB: Il est parfois nécessaire de créer un compte ftp, l'absence de l'option *system* crée une faille de sécurité et bloque la désinstallation du paquet.

        sudo useradd --system ftp
        Pensez à redémarrer le service :

        sudo systemctl restart vsftpd
        Vérifier l'état du service.

        sudo systemctl status vsftpd
        sudo systemctl enable vsftpd
        ENSUITE, penser a ouvrir les ports de votre pare-feu si nécessaire  avec :

                    sudo ufw allow 20/tcp
                    sudo ufw allow 21/tcp
                    sudo ufw status

3.CONFIGURATION
  La configuration de VsFTPd est centralisée dans un seul et même fichier /etc/vsftpd.conf. Choisissez votre éditeur de texte favori (en mode super utilisateur) et appliquez les modifications suivantes en fonction du mode de fonctionnement de VsFTPd. 


Et voilà, votre serveur est maintenant installé 👍
