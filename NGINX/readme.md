1.Qu'est-ce que c'est NGINX 
    Nginx, prononcé comme « engine-ex », est un serveur web open-source qui, depuis son succès initial en tant que serveur web, est maintenant aussi utilisé comme reverse proxy, cache HTTP, et load balancer.

2.Comment fonctionne Nginx ?
    Nginx est conçu pour offrir une faible utilisation de la mémoire et une grande simultanéité. Plutôt que de créer de nouveaux processus pour chaque requête Web, Nginx utilise une approche asynchrone et événementielle où les requêtes sont traitées dans un seul thread.

3.Installation de NGINX
    Pour se faire , il suffit de teper la commande suivante : "apt-get install nginx "
    Et afin de verifier cette installation , il faut taper "whereis nginx" puis pour verifier on execute "sudo systemctl start nginx "
    

4.Configuration de NGINX
    Il est à noter que tpus les fichiers de configurationd de NGINX se trouve dans "./etc/nginx/nginx.conf "
    Et elle peut être modifié afin de changé la configuration global par "./etc/nginx/sites-available/"(repertoit dans le répertoire dans lequel vous pouvez stocker les blocs de serveur par site.)
Nginx n’utilisera pas les fichiers de configuration trouvés dans ce répertoire à moins qu’ils ne soient liés au répertoire sites-enabled. En règle générale, la configuration de tous les blocs de serveur se fait dans ce répertoire, puis s’active en établissant une liaison avec l’autre répertoire.

./etc/nginx/sites-enabled/: répertoire dans lequel les blocs de serveur par site activés sont stockés.
En règle générale, ils sont créés en reliant les fichiers de configuration trouvés dans le répertoire sites-available.

./etc/nginx/snippets: ce répertoire contient des fragments de configuration qui peuvent être inclus ailleurs dans la configuration Nginx. Les segments de configuration potentiellement reproductibles sont de bons candidats pour la refactorisation en fragments.

Félicitations !... Vous avez réussi à installer NGINX 👏
