# TP-1

## Exercice 2

### Manuel

#### A l'aide du manuel, identifiez le rôle de la commande which
1. La commande which affiche le chemin complet d'un executable, elle recherche ce chemin dans les répertoires indiqués dans l'option PATH.
#### Quand on consulte une page du manuel, comment peut-on rechercher un terme (par exemple, chercherle termeoptiondans la page de manuel dewhich?
2.  On recherche un terme en faisant `/nomDuTerme`.
#### Comment quitte-t-on le manuel?
3. On quitte le manuel avec la touche `q`.
#### Chaque section du manuel a une première page, qui présente le contenu de la section. Aﬀicher lapremière page de la section 6; de quoi parle cette section?
4. On accède via la commande : `man 6 intro`
La section 6 parle de jeux vidéos et de petits programmes disponibles sur l'OS.

### Navigation dans l'arborescence des fichiers
#### allez dans le dossier /var/log
1. faire la commande -> cd `/var/log`.
#### remontez dans le dossier parent (/var) en utilisant un chemin relatif
2. faire la commande -> `cd ..` .
#### retournez dans le dossier personnel
3. faire la commande -> `cd /home/louis` .
#### revenez au dossier précédent (/var) sans utiliser de chemin
4. faire la commande -> : `cd -` .
#### essayez d’accéder au dossier /root; que se passe-t-il?
5. C'est impossible d'accéder au dossier /root car l'utilisateur n'a pas les droits nécessaires .
#### essayez la commande sudo cd /root; que se passe-t-il? Expliquez
6. La commande ne fonctionne pas car sudo fonctionne pour l’exécution des programmes et cd n'est pas un programme.
#### à partir de votre dossier personnel, créez l’arborescence suivante :
7. Liste des commandes :
 -> `mkdir Dossier1`
 -> `touch Dossier1 Fichier1`
 -> `mkdir Dossier2`
 -> `mkdir Dossier2/Dossier2.1`
 -> `mkdir Dossier2/Dossier2.2`
 -> `touch Dossier2/Dossier2.2/Fichier2`
 -> `touch Dossier2/Dossier2.2/Fichier3`
 #### revenez dans votre dossier personnel; à l’aide de la commande rm, essayez de supprimer Fichier1, puis Dossier1; que se passe-t-il?
 8. On ne peut pas supprimer le fichier1 a l'aide de rm il va falloir utiliser l'option -r si on veut supprimer dossier1 et fichier1 .
 #### quelle commande permet de supprimer un dossier?
 9. faire la commande -> `rmdir Dossier1` .
 #### que se passe-t-il quand on applique cette commande à Dossier2?
 10. On ne peut pas supprimer le dossier2 a l'aide de la commande rmdir car le dossier n'est pas vide .
 #### comment supprimer en une seule commande Dossier2 et son contenu?
 11. Pour supprimer un dossier avec un contenu il faudra utiliser la commande `rm -r` .

### Commandes importantes
#### Quelle commande permet d’aﬀicher l’heure? A quoi sert la commandetime?
1. faire la commande ->  `date` .
La commande time permet de chronométrer le temps d'exécution d'une tache.
#### Dans votre dossier personnel, tapez successivement les commandes ls puis la; que peut-on en déduire sur les fichiers commençant par un point?
2. Les fichiers avec un point sont des fichiers cachés.
#### Où se situe le programme ls?
3. On utilise la commande `which ls` pour trouver l'emplacement, il se situe dans "usr/bin/ls".
#### Essayez la commande ll. Existe-t-il une entrée de manuel pour cette commande? Utilisez les commandes alias ou alias pour en savoir plus sur la nature de cette commande.
4. Non il n'y a pas d'entrée manuel pour "ll" .
La commande "ll" est un alias pour "ls -alF".
- L'option "a" permet de lister tout ce qu'il y a dans le répertoire
- L'option "l" permet d'utiliser un format long pour l'affichage.
- L'option "F" permet de formater la liste.
#### Quelle commande permet d’aﬀicher les fichiers contenus dans le dossier /bin?
5. faire la commande -> `ls /bin`.
#### Que fait la commandels ..?
6. La commande "ls .." permet d'afficher tous les fichiers présents dans le répertoire du dossier courant.
#### Quelle commande donne le chemin complet du dossier courant?
7. faire la commande -> `pwd`.
#### Que fait la commande echo 'yo' > plop exécutée 2 fois?
8. cette commande va créer un fichier plop ou il va écrire yo une fois car la deuxième fois sera réécri sur l'ancien yo.
A chaque exécution le fichier est écrasé.
#### Que fait la commande echo 'yo' >> plop exécutée 2 fois?
9. Cette commande permet d'afficher deux fois yo au debut et a la fin un autre yo, dans ce cas il ne sera pas écrasé.
#### Interprétez le comportement de la commandesleep 10 | echo 'toto'?
10. La commande écrit "toto" et attend 10 secondes avant de redonner la main à l'utilisateur.
#### A quoi sert la commande file? Essayez la sur des fichiers de types différents.
11. Cela permet de connaître le type du fichier (directory / ASCII text ...).
#### Créez un fichier toto qui contient la chaîne Hello Toto !; créer ensuite un lien titi vers ce fichier avec la commande ln toto titi. Modifiez à présent le contenu de toto et aﬀichez le contenu de titi:qu’observe-t-on? Supprimez le fichier toto; quelle conséquence cela a-t-il sur titi?
12. Lorsqu'on modifie toto, le fichier titi est aussi modifié. Cela n'a aucune conséquence sur le fichier titi que toto soit supprimé.
#### Créez à présent un lien symbolique tutu sur titi avec la commande ln -s titi tutu. Modifiez le contenu de titi; quelle conséquence pour tutu? Et inversement? Supprimez le fichier titi; quelle conséquence cela a-t-il sur tutu?
13. Lorsqu'on modifie titi, tutu est aussi modifié.
A l'inverse en modifiant tutu cela n'a pas d'impacte sur titi. 
Si on supprime le fichier titi, tutu va perdre tout son contenu.
#### Aﬀichez à l’écran le fichier /var/log/syslog. Quels raccourcis clavier permettent d’interrompre et reprendre le défilement à l’écran?
14. faire la commande -> `CTRL + S` pour stopper le défilement ou la touche 'arret defil' sur certain clavier.
faire la commande ->  `CTRL + Q` pour reprendre le défilement.
#### Aﬀichez les 5 premières lignes du fichier /var/log/syslog, puis les 15 dernières, puis seulement les lignes 10 à 20.
15. faire la commande ->  `head -5 /var/log/syslog` pour afficher les 5 premières lignes.
Pour les  15 dernières faire la commande ->  `tail -15 /var/log/syslog` .
#### Que fait la commande dmesg | less?
16. La commande dmesg permet d'afficher le tampon de la machine. 
La commande less permet de defiler lentement a chaque 'entrer'.
#### Aﬀichez à l’écran le fichier /etc/passwd; que contient-il? Quelle commande permet d’aﬀicher la pagede manuel de ce fichier?
17. Elle affiche la liste des utilisateurs ainsi que leur groupe et les fichiers dont ils sont propriétaires.
#### Aﬀichez seulement la première colonne triée par ordre alphabétique inverse
18. faire la commande -> `cat /etc/passwd | cut -d: -f1 | sort -r` (sort -r marche pas)
#### Quelle commande nous donne le nombre d’utilisateurs ayant un compte sur cette machine (pas seule-ment les utilisateurs connectés)?
19. faire la commande -> `wc -l /etc/passwd`.
#### Combien de pages de manuel comportent le mot-clé conversion dans leur description?
20. 3 page du manuel comportent le mot-clé conversion.
faire la commande -> ` man -k conversion | wc -l`
#### A l’aide de la commande find, recherchez tous les fichiers se nommant passwd présents sur la machine
21. faire la commande -> `find / -name passwd`
#### Modifiez la commande précédente pour que la liste des fichiers trouvés soit enregistrée dans le fichier ~/list_passwd_files.txt et que les erreurs soient redirigées vers le fichier spécial /dev/null
22. La commande est : `sudo find / -name passwd > ~/list_passwd_files.txt 2> /dev/null`
#### Dans votre dossier personnel, utilisez la commande grep pour chercher où est défini l’alias ll vu précédemment
23. 
#### Utilisez la commande locate pour trouver le fichier history.log.
24.  En utilisant la commande `locate history.log`, on obtient le chemin /var/log/apt/history.log
#### Créer un fichier dans votre dossier personnel puis utilisez locate pour le trouver. Apparaît-il? Pourquoi?
25. "locate" ne permet pas de trouver le fichier créé car il se base sur une liste de fichiers fixe.

### Exercice 4. Personnalisation du shell
#### Le fichier.bashrc est lu au démarrage du shell; pour le recharger, il faudrait donc se déconnecter puis se reconnecter; mais il existe un autre moyen : la commande source .bashrc. Testez-la, l’invite de commande devrait immédiatement passer en couleurs.
3. En utilisant la commande source .bashrc le shell passe bien en couleur.
#### Les couleurs par défauts (surtout celle du dossier courant) ne sont pas très visibles. Dans .bashrc,cherchez les lignes commençant par PS1=; elles indiquent la mise en forme de l’invite de commande(selon que l’on est en couleurs ou non).
4. La ligne qui permet cet affichage est : 'PS1='${debian_chroot:+($debian_chroot)}\[\[\033[35m\][\A]\[\033[30m\] - \[\033[01;32m\]\u@\h\[\033[00m\]:\[\033[01;36m\]\w\[\033[00m\]\$ ''
