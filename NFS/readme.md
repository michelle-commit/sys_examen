1.DESCRIPTION (NFS)
    Le NFS, Network File System, que l'on pourrait traduire par "Système de fichiers en réseau", est un protocole de transferts de fichiers par le réseau principalement utilisé sur les systèmes Linux/Unix,
    même s'il est compatible avec Windows et MacOS. 
    
    2.INSTALLATION
Ici, on va voir l'installation d'un serveur NFS et montrer comment connecter un client à ce partage.
Tout d'abord mettons à jour notre systeme avec "apt udate "

Puis , l'installation se poursuit par :$ apt install nfs-kernel-server

3.CONFIGURATION
   Pour la paverrtie cliente, on installe les paquets adéquats :

$ apt install nfs-common $ mkdir -p /media/nfs mount -t nfs 192.168.21.200:/media/partage /media/nfs

Avec la commande df, on peut voir que tout est monté :

$ df -h Filesystem Size Used Avail Use% Mounted on 192.168.21.200:/media/partage 20G 985M 18G 5% /media/nfs


Et voilà, votre serveur est maintenant installé 👍
