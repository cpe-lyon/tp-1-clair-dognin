# Compte rendu :  TP1 Administration Système

## Clair Mathias et Dognin Alexis
### Date: 06/02/2020

**EXERCICE 2:**  Prise en main de l'interpréteur de commandes 
**Manuel**
1. A l’aide du manuel, identifiez le rôle de la commande which:
	*La commande **which** renvoie le chemin de l'emplacement de la commande*
2. Quand on consulte une page du manuel, comment peut-on rechercher un terme (par exemple, chercher le terme option dans la page de manuel de which?:
	*On utilise le **/** suivi de l'expression à retrouver, par exemple **/options***
3. Comment quitte-t-on le manuel?:
	*On appuye sur la touche **q***
4. Chaque section du manuel a une première page, qui présente le contenu de la section. Aﬀicher la première page de la section. 
De quoi parle cette section?:
*Cette section parle des différents jeux et programmes amusants qui se trouvent dans le système*
&NewLine;

**Navigation dans l'arborescence**

1. Allez dans le dossier /var/log:
	*On utilise la commande **cd /var/log** pour aller dans ce dossier. Pour avancer dans une arborescence on utilise la commande **cd** de manière générale*
2. Remontez dans le dossier parent (/var) en utilisant un chemin relatif.:
	*On utilise la commande **cd . .***
3. Retournez dans le dossier personnel:
		*On utilise la commande **cd***
4. Revenez au dossier précédent (/var)sans utiliser de chemin:
		*On utilise la commande **cd - -***
5. Essayez d’accéder au dossier /root; que se passe-t-il?:
	*L'accès est refusé*
6. Essayez la commande sudo cd /root; que se passe-t-il? Expliquez:
	***sudo** permet d'emprunter les privilèges admnistrateur pour exécuter une commande donc la commande fonctionne*
7. A partir de votre dossier personnel, créez l’arborescence suivante :
	*Pour créer cette arborescence on utilise **sudo mkdir "nomDossier"** et **sudo echo > "nomFichier***
8. Revenez dans votre dossier personnel; à l’aide de la commande rm, essayez de supprimer Fichier1, puisDossier1; Que se passe-t-il?:
	*En utilisant **sudo** on arrive à supprimer le fichier mais pas le dossier.*
9. Quelle commande permet de supprimer un dossier?:
	*On doit rajouter **-r** pour  supprimer un dossier.*
10. Que se passe-t-il quand on applique cette commande à Dossier2?:
	*Tout le dossier 2 et son contenu est supprimé.*
11. Comment supprimer en une seule commande Dossier2 et son contenu?: 
	*Avec la ligne de commande vu au-dessus*
&NewLine;
 
**Commandes importantes**

1. Quelle commande permet d’aﬀicher l’heure? A quoi sert la commande time?: 
	*La commande **date** permet d'afficher l'heure et la commande **time** permet de calculer le temps d'execution d'une commande* 
2. Dans votre dossier personnel, tapez successivement les commandes ls puis la; que peut-on en déduire sur les fichiers commençant par un point?:
	*Les fichiers commençant par un . sont des fichiers cachés* 
3. Où se situe le programme ls?:
	*On utilise **which ls** et on obtient /usr/bin/ls*
4. Essayez la commande ll. Existe-t-il une entrée de manuel pour cette commande? Utilisez les commandes alias ou alias pour en savoir plus sur la nature de cette commande.:
	*Non il n'y a pas d'entrée de manuel pour cette commande. C'est une abrégée pour la commande ls -alF*
5. Quelle commande permet d’aﬀicher les fichiers contenus dans le dossier/bin?:
	*ls /bin*
6. Que fait la commande ls ..?:
	*Elle affiche les fichiers du dossier parent*
7. Quelle commande donne le chemin complet du dossier courant?:
	*La commande pwd*
8. Que fait la commande echo 'yo' > plop exécutée 2 fois?:
	*La première fois, elle crée un fichier plop dont le contenu est yo, et la seconde fois elle écrase le contenu du fichier plop avec yo*
9. Que fait la commande echo 'yo' >> plop exécutée 2 fois?:
	*Elle ajoute deux yo au fichier plop*
10. A quoi sert la commande file? Essayez la sur des fichiers de types différents.:
	*Elle donne des informations sur l'encodage des caractères du fichier*
11. Créez un fichier toto qui contient la chaîne Hello Toto !; créer ensuite un lien titi vers ce fichier avec la commande ln toto titi. Modifiez à présent le contenu de toto et aﬀichez le contenu de titi:qu’observe-t-on? Supprimez le fichier toto; quelle conséquence cela a-t-il sur titi?:
	*titi change quand toto change. Lorsque toto est supprimé, on a toujours titi*
12. Créez à présent un lien symbolique tutu sur titi avec la commande ln -s titi tutu. Modifiez le contenu de titi; quelle conséquence pour tutu? Et inversement? Supprimez le fichier titi; quelle conséquence cela a-t-il sur tutu?:
	*tutu change quand titi change. tutu est supprimé quand titi est supprimé*
13. Aﬀichez à l’écran le fichier/var/log/syslog. Quels raccourcis clavier permettent d’interrompre et reprendre le défilement à l’écran?:
		*Pour mettre en pause on utilise **Ctrl+S** et pour reprendre **Ctrl+Q***
14. Aﬀichez les 5 premières lignes du fichier/var/log/syslog, puis les 15 dernières, puis seulement les lignes 10 à 20.:
	*On utilise **sed -n [ligne_debut],[ligne_fin]p nom_du_fichier***
15. Que fait la commande dmesg | less?:
	*La commande permet d'afficher les buffers, le **less** permet d'afficher une page à la fois*
16. Aﬀichez à l’écran le fichier/etc/passwd; que contient-il? Quelle commande permet d’aﬀicher la page de manuel de ce fichier?:
	*Il contient la liste des comptes sur el système et des informations sur ce compte. Pour avoir des infos, on utilise **man passwd***
17. Aﬀichez seulement la première colonne triée par ordre alphabétique inverse:
18. Quelle commande nous donne le nombre d’utilisateurs ayant un compte sur cette machine (pas seule-ment les utilisateurs connectés)? 
		*La commande est **cat -n etc/passwd***
19. Combien de pages de manuel comportent le mot-clé conversion dans leur description?:
20. A l’aide de la commande find, recherchez tous les fichiers se nommant passwd présents sur la machine:
		*On utilise la comande **sudo find -name passwd***
21. Modifiez la commande précédente pour que la liste des fichiers trouvés soit enregistrée dans le fichier~/list_passwd_files.txtet que les erreurs soient redirigées vers le fichier spécial/dev/null:
22. Dans votre dossier personnel, utilisez la commande grep pour chercher où est défini l’alias ll vu précédemment:
23. Utilisez la commande locate pour trouver le fichierhistory.log.:
	*On fait **locate history.log** et on obtient **/var/log/apt/history.log***
24. Créer un fichier dans votre dossier personnel puis utilisez locate pour le trouver. Apparaît-il? Pourquoi?:
	*Il n'apparaît pas parce qu'il n'est pas dans les databases de la fonction **locate***


**EXERCICE 4:** Personnalisation du shell 
&NewLine;
*On veut personnaliser notre shell.
On utilise Nano pour rentrer dans le fichier .bashrc
Une fois que la ligne **force_color_prompt=yes** est décommenté, on peut modifier les couleurs de notre shell.
On modifie les couleurs afin d'avoir le format voulu, et on rajoute les mot clefs pour avoir l'heure et le path d'execution.*
