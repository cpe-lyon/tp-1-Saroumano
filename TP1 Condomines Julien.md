# 			TP1 Condomines Julien



## Exercice 2



### Manuel

1. On cherche tout d'abord à comprendre l'utilité de la commande which, on va donc rentrer la commande -man which, celle ci nous permettra donc d'obtenir le chemin ou les fichiers qui seront exécuter en cas de commandes. 
2. Si l'on souhaite faire une recherche à l'intérieur du manuel, ici option on utilise la commande -find
3. Si l'on souhaite quitter la page du manuel, il faut faut presser la touche -q.
4. L'introduction de la section 6 nous annonce que c'est dans cette même section que nous pourrons retrouver les jeux et les programmes non essentielles. 


### Navigation dans l’arborescence des fichiers
1. On va tout d'abord utiliser la commande -cd /var/log pour ce rendre dans le fichier voulu.
2. Pour revenir au /var en utilisant un chemin relatif il faut utiliser la commande  -cd -.. 
3. On utilise la commande -cd ~/ pour retourner directement à la racine 
4. On utilise la commande -cd - pour retourner au dossier dans lequel on travaillait précédemment.
5. Lorsque l'on souhaite accéder au dossier /root, un message d'erreur s'affiche nous indiquant que nous n'avons pas les permissions nécessaire. 
6. Lorsque nous essayons de lancer la commande -sudo cd /root, un message d'erreur indique que la commmande cd est introuvable, cela est dûe au faite que la commande cd est une commande faite pour le shell, interne à Bash et qu'elle ne peut donc pas être lancé directement à l'aide de la commande sudo.
7. Pour créer un dossier, il faut utiliser la commande -mkdir et renseigner le nom que l'on veut donner au dossier. On se rend ensuite dans le dossier en question à l'aide de la commande cd, puis à l'aide de la commande -touch suivi du nom que l'on veut donner au fichier.cd
8. Depuis notre dossier personnel, en utilisant la commande -rm précédé du chemin définis à l'aide de la commande -cd, il est possible de supprimer le fichier1. Cependant, la même commande ne fonctionnera pas pour le Dossier1 un message d'erreur apparaitra nous indiquant que l'on ne peut le supprimer car c'est un dossier. 
9. Afin de supprimer un dossier il faut utiliser la commande -rmdir;
10. Un message d'erreur apparait indiquant qu'il est impossible de supprimer le dossier car il contient des sous dossier.
11. Il faut utiliser la commande -rm rf afin de supprimer l'ensemble du dossier et de son sous dossier.


### Commandes importantes

1. Afin d'afficher uniquement la date, on peut utiliser la commande -date %t.
2. 
3. Il faut utiliser la commande -realpath suivi du nom de la commande
4. z
5. On peut utiliser la commande ls /bin pour afficher le contenu du dossier
6. La commande ls .. présente l'ensemble des dossier présents dans le répertoire ainsi que les fichiers qu'ils contiennent.
7. On peut utiliser la commande pwd pour avoir accès au chemin complet du dossier courant 
8. z
9. z
10. La commande sleep 10 va faire temporiser pendant 10 seconde le départ de la commande echo 'toto'.
11. La commande file est utilisée pour déterminer le type du fichier sélectionné.
12. z
13. z
14. Le raccourci clavier permettant d'arreter le défilement est Ctrl + z
15. 
