# 			TP1 Condomines Julien

## Exercice 2. Prise en main de l’interpréteur de commandes
	
### Manuel
	
#### Question 1 : A l’aide du manuel, identifiez le rôle de la commande which
La commande ```which``` renvoie le chemin des fichiers (ou liens) qui seraient éxécutés dans l'environnement courant si ddes arguments avaient été données comme commandes dans un interpréteur de commandes strictement conforme à POSIX. pour ce faire, ```which``` cherche dans la variable PATH les fichiers éxécutables correspondant aux noms des arguments. ```which``` ne normalise pas les chemins.
		
#### Question 2 : Quand on consulte une page du manuel, comment peut-on rechercher un terme (par exemple, chercher le terme option dans la page de manuel de which ?
Lorsque l'on a tapé ```man which``` on tape ensuite ```/options```.
		
#### Question 3 : Comment quitte-t-on le manuel ?
On quitte le manuel en pressant la touche "q".
	
#### Question 4 : Afficher la première page de la section 6 ; de quoi parle cette section ?
On tape la commande ```man 6 intro```.
			
### Navigation dans l’arborescence des fichiers
	
#### Question 1 : allez dans le dossier /var/log
On tape la commande ```cd /var/log```.
		
#### Question 2 : remontez dans le dossier parent (/var) en utilisant un chemin relatif
On éxécute la commande ```cd ..```.
		
#### Question 3 : retournez dans le dossier personnel
On éxécute la commande ```cd ~```.
		
#### Question 4 : revenez au dossier précédent (/var)
On éxécute la commande ```cd /var```.
		
#### Question 5 : essayez d’accéder au dossier /root ; que se passe-t-il ?
On obtient une erreur système : "permission denied".
		
#### Question 6 : essayez la commande sudo cd /root ; que se passe-t-il ? Expliquez
On nous demande de saisir le mdp admin mais au final on obtient un "command not found". La commande ```sudo``` n'est disponible qu'en bash.
		
#### Question 7 : à partir de votre dossier personnel, créez l’arborescence suivante :
```bash
mkdir Dossier1 Dossier2 Dossier2/Dossier2.1 Dossier2/Dossier2.2
touch Dossier1/Fichier1 Dossier2/Dossier2.2/Fichier2 Dossier2/Dossier2.2/Fichier3
``` 
		
#### Question 8 : revenez dans votre dossier personnel ; à l’aide de la commande rm, essayez de supprimer Fichier1, puis Dossier1 ; que se passe-t-il ?
Ca ne le supprime pas car le dossier n'est pas vide.
	
#### Question 9 : quelle commande permet de supprimer un dossier ?
Il suffit de saisir ```rmdir``` pour supprimer le dossier vide.

#### Question 10 : que se passe-t-il quand on applique cette commande à Dossier2 ?
Le dossier n'est pas supprimé car il n'est pas vide.

#### Question 11 : comment supprimer en une seule commande Dossier2 et son contenu ?
Il suffit de saisir ```rm -rf``` pour supprimer le dossier (et son contenu).


### Commandes importantes
	
#### Question1 : Quelle commande permet d’afficher l’heure ? A quoi sert la commande time ?
Il suffit de saisir ```date +%T```. ```time``` renvoie l'heure actuelle sous forme du nombre de secondes écoulées depuis le 1er janvier 1970 à 00h 00m 00s GMT, le début de l'Ère Unix.
		
#### Question2 : Dans votre dossier personnel, tapez successivement les commandes ls puis la ; que peut-on en déduire sur les fichiers commençant par un point ?
Les fichiers commençant par un point sont des fichiers cachés.
		
#### Question3 : Où se situe le programme ls ?
Grace à la commande ```whereis ls``` on voit qu'il est situé dans le dossier /bin/ls /usr/share/man/man1/ls.1.gz
		
#### Question 4 : Que fait la commande ll ? . Existe-t-il une entrée de manuel pour cette commande ? Utilisez les commandes alias ou alias pour en savoir plus sur la nature de cette commande.
Elle permet de lister tout le contenu présent dans le répertoire actuel (avec des données supplémentaires tel que les droits).
		
#### Question 5 : Quelle commande permet d’afficher les fichiers contenus dans le dossier /bin ?
Grace à la commande ```ls /bin```.
		
#### Question 6 : Que fait la commande ls .. ?
Elle affiche le contenu du dossier parent.
		
#### Question 7 : Quelle commande donne le chemin complet du dossier courant ?
Grace à la commande ```pwd```.
		
#### Question 8 : Que fait la commande echo 'bip' > plop exécutée 2 fois ?
La première éxécution de commande permet d'écrire "bip" dans le fichier plop (il est créé s'il n'existe pas) et la seconde commande va écraser le contenu du fichier.
		
#### Question 9 : Que fait la commande echo 'bip' >> plop exécutée 2 fois ?
La première éxécution de commande permet d'écrire "bip" dans le fichier plop (il est créé s'il n'existe pas) et la seconde commande va rajouter le texte "bip" à la fin du fichier.
		
#### Question 11 : A quoi sert la commande file ? Essayez la sur des fichiers de types différents.
La commande ```file``` permet gràce à ses tests de déterminer le type de fichier présent en utilisant les metadonnées du fichier sans se soucier de l'extension (ASCCI, empty...).
		
#### Question 12 : Créez un fichier original qui contient la chaîne Hello Toto ! ; créer ensuite un lien lien_phy vers ce fichier avec la commande ln original lien_phy. Modifiez à présent le contenu de original et affichez le contenu de lien_phy : qu’observe-t-on ? Supprimez le fichier original ; quelle conséquence cela a-t-il sur lien_phy ?
En affichant le contenu de lien_phy on observe exactement le même contenu que celui de original.
En supprimant le fichier original le lien s'est rompu et lien_phy existe toujours avec son contenu.
		
#### Question 13 : Créez à présent un lien symbolique lien_sym sur lien_phy avec la commande ln -s lien_phy lien_sym. Modifiez le contenu de lien_phy ; quelle conséquence pour lien_sym ? Et inversement ? Supprimez le fichier lien_phy ; quelle conséquence cela a-t-il sur lien_sym ?
On peut créer du contenu dans les 2 fichiers à partir de l'un ou de l'autre. Mais une fois l'un des fichiers supprimé le lien se rompt définitivement et le contenu est supprimé.
		
#### Question 14 : Affichez à l’écran le fichier /var/log/syslog. Quels raccourcis clavier permettent d’interrompre et reprendre le défilement à l’écran ?
Il faut taper la commande ```ctrl+Z``` et de taper ```bg``` pour déplacer le processus en background.
	
#### Question 15 : Affichez les 5 premières lignes du fichier /var/log/syslog, puis les 15 dernières, puis seulement les lignes 10 à 20.
Il faut exécuter ```head -5 /var/log/syslog```  
Il faut exécuter ```tail -15 /var/log/syslog```  
Il faut exécuter ```sed -n 10,20p /var/log/syslog```  
		
#### Question 16 : Que fait la commande dmesg | less ?
La commande ```dmesg``` affiche le buffer du noyau.
L'option ```less``` permet d'afficher le contenu page par page et permet de naviguer.
		
#### Question 17 : Affichez à l’écran le fichier /etc/passwd ; que contient-il ? Quelle commande permet d’afficher la page de manuel de ce fichier ?
Le fichier "/etc/passwd" contient les mots de passe cryptés des utilisateurs.
		
#### Question 18 : Affichez seulement la première colonne triée par ordre alphabétique inverse
Pour afficher la première colonne du fichier "/etc/passwd" triée par ordre alphabétique inverse, il faut taper respectivement les 2 commandes suivantes : 
```bash
cut -c1 /etc/passwd > toto.txt
sort -r toto.txt
```
		
#### Question 19 : Quelle commande nous donne le nombre d’utilisateurs ?
La commande ```wc -l /etc/passwd``` permet de compter le nombre de lignes du fichier, et donc le nombre d'utilisateurs.
		
#### Question 20 : Combien de pages de manuel comportent le mot-clé conversion dans leur description ?
La commande ```man -k conversion | wc -1``` permet d'afficher les pages du manuel comportant le mot "conversion"
		
#### Question 21 : A l’aide de la commande find, recherchez tous les fichiers se nommant passwd présents sur la machine
La commande ```find -name passwd``` permet de rechercher tous les fichiers se nommant passwd
		
#### Question 22 : Modifiez la commande précédente pour que la liste des fichiers trouvés soit enregistrée dans le fichier ~/list_passwd_files.txt et que les erreurs soient redirigées vers le fichier spécial /dev/null
La commande ```find -name passwd > list_passwd_files.text 2> /dev/null``` permet de rechercher tous les fichiers nommé passwd. ">" permet de sauver les recherche dans le fichier nommé ensuite et 2> permet de sauver les erreurs.
	
#### Question 23 : Dans votre dossier personnel, utilisez la commande grep pour chercher où est défini l’alias ll vu précédemment
La commande ```grep 'alias ll'``` permet de retrouver l'alias.
	
#### Question 24 : Utilisez la commande locate pour trouver le fichier history.log.
		
#### Question 25 : Créer un fichier dans votre dossier personnel puis utilisez locate pour le trouver. Apparaît-il ? Pourquoi ? 
La commande ```locate history.log``` permet de trouver le log history. On ne trouve pas le fichier créé dans le dossier personnel avec la commande "locate" puisque le fichier n'a pas été ajouté à la base de donnée que parcourt la commande locate. Il faut raffraichir cette base de donnée pour afficher le dossier.

## Exercice 3. Découverte de l’éditeur de texte nano


## Exercice 4. Personnalisation du shell
	
La commande ```source .bashrc``` permet de recharger le fichier .bashrc.  
Afin d'obtenir le même affichage que l'énnoncé, on utilise la commande : 
```bash
PS1='${debian_chroot:+($debian_chroot)}[\033[35m]\A[\033[00m]-[\033[01;92m]\u@\h[\033[00m]:[\033[94m]\w[\033[00m]$'
```
