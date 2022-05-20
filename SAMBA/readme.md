1-DESCRIPTION DE SAMBA 
    Un serveur Samba est caractérisé comme tel lorsqu’une suite de logiciels gratuits est utilisée pour partager les ressources de systèmes incompatibles par nature. La licence publique générale GNU permet l’implantation du protocole SMB (Server Message Block), qui a donné le nom à la suite Samba, dans les systèmes d’exploitation Linux et Unix.
    
    
2. Ses fonctions 
    Partager un disque Linux pour des machines Windows
Partager une imprimante Linux avec des machines Windows
Partager une imprimante Windows à partir d’un hôte LinuxGérer des listes de machines présentes sur le réseau et leur mise à disposition pour tous types de clients (cf : voisinage réseau)


3. Comment installer samba sur linux 
    Utiliser la commande suivante : 
    $ sudo apt-get install samba 
    
    
4.LES comptes à installer avec samba
    Après l'installation de "SAMBA" , il faut aussi installer  la commande smbpasswd suivante car elle est controlée par l’administration des comptes utilisateurs . Cette commande est comprend quatre paramètres a, x, d et e représentés par leurs lignes de commandes respectives comme ci-dessous :
    -$ sudo smbpasswd -a NOM UTILISATEUR (MOT DE PASSE)

    -$ sudo smbpasswd -x NOM UTILISATEUR

    -$ sudo smbpasswd -d NOM UTILISATEUR

    -$ sudo smbpasswd -e NOMU TILISATEUR  
  NB: Le serveur peut charger et prendre en compte toutes les modifications effectuées grâce à la commande suivante :
  $ sudo service smbd reload
  
5.Configuration de samba
    Si vous souhaitez par exemple partager un dossier avec des photos et autorisant des ajouts et modifications d’autres utilisateurs, vous pouvez configurer ces paramètres avec les commandes suivantes :

    [Photos]

    path= /documents/photos

    writeable = yes

    guest ok = yes

    Pour l'autorisation, il suffit de taper la commande:
    $ chmod 777 [le nom de dossier]  
Ainsi s'achève notre travaille , maintenant vous savez tous ce qu'il y a à savoir sur SAMBA
