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


## Rename a file

You can rename the current file by clicking the file name in the navigation bar or by clicking the **Rename** button in the file explorer.

## Delete a file

You can delete the current file by clicking the **Remove** button in the file explorer. The file will be moved into the **Trash** folder and automatically deleted after 7 days of inactivity.

## Export a file

You can export the current file by clicking **Export to disk** in the menu. You can choose to export the file as plain Markdown, as HTML using a Handlebars template or as a PDF.


# Synchronization

Synchronization is one of the biggest features of StackEdit. It enables you to synchronize any file in your workspace with other files stored in your **Google Drive**, your **Dropbox** and your **GitHub** accounts. This allows you to keep writing on other devices, collaborate with people you share the file with, integrate easily into your workflow... The synchronization mechanism takes place every minute in the background, downloading, merging, and uploading file modifications.

There are two types of synchronization and they can complement each other:

- The workspace synchronization will sync all your files, folders and settings automatically. This will allow you to fetch your workspace on any other device.
	> To start syncing your workspace, just sign in with Google in the menu.

- The file synchronization will keep one file of the workspace synced with one or multiple files in **Google Drive**, **Dropbox** or **GitHub**.
	> Before starting to sync files, you must link an account in the **Synchronize** sub-menu.

## Open a file

You can open a file from **Google Drive**, **Dropbox** or **GitHub** by opening the **Synchronize** sub-menu and clicking **Open from**. Once opened in the workspace, any modification in the file will be automatically synced.

## Save a file

You can save any file of the workspace to **Google Drive**, **Dropbox** or **GitHub** by opening the **Synchronize** sub-menu and clicking **Save on**. Even if a file in the workspace is already synced, you can save it to another location. StackEdit can sync one file with multiple locations and accounts.

## Synchronize a file

Once your file is linked to a synchronized location, StackEdit will periodically synchronize it by downloading/uploading any modification. A merge will be performed if necessary and conflicts will be resolved.

If you just have modified your file and you want to force syncing, click the **Synchronize now** button in the navigation bar.

> **Note:** The **Synchronize now** button is disabled if you have no file to synchronize.

## Manage file synchronization

Since one file can be synced with multiple locations, you can list and manage synchronized locations by clicking **File synchronization** in the **Synchronize** sub-menu. This allows you to list and remove synchronized locations that are linked to your file.


# Publication

Publishing in StackEdit makes it simple for you to publish online your files. Once you're happy with a file, you can publish it to different hosting platforms like **Blogger**, **Dropbox**, **Gist**, **GitHub**, **Google Drive**, **WordPress** and **Zendesk**. With [Handlebars templates](http://handlebarsjs.com/), you have full control over what you export.

> Before starting to publish, you must link an account in the **Publish** sub-menu.

## Publish a File

You can publish your file by opening the **Publish** sub-menu and by clicking **Publish to**. For some locations, you can choose between the following formats:

- Markdown: publish the Markdown text on a website that can interpret it (**GitHub** for instance),
- HTML: publish the file converted to HTML via a Handlebars template (on a blog for example).

## Update a publication

After publishing, StackEdit keeps your file linked to that publication which makes it easy for you to re-publish it. Once you have modified your file and you want to update your publication, click on the **Publish now** button in the navigation bar.

> **Note:** The **Publish now** button is disabled if your file has not been published yet.

## Manage file publication

Since one file can be published to multiple locations, you can list and manage publish locations by clicking **File publication** in the **Publish** sub-menu. This allows you to list and remove publication locations that are linked to your file.


# Markdown extensions

StackEdit extends the standard Markdown syntax by adding extra **Markdown extensions**, providing you with some nice features.

> **ProTip:** You can disable any **Markdown extension** in the **File properties** dialog.


## SmartyPants

SmartyPants converts ASCII punctuation characters into "smart" typographic punctuation HTML entities. For example:

|                |ASCII                          |HTML                         |
|----------------|-------------------------------|-----------------------------|
|Single backticks|`'Isn't this fun?'`            |'Isn't this fun?'            |
|Quotes          |`"Isn't this fun?"`            |"Isn't this fun?"            |
|Dashes          |`-- is en-dash, --- is em-dash`|-- is en-dash, --- is em-dash|


## KaTeX

You can render LaTeX mathematical expressions using [KaTeX](https://khan.github.io/KaTeX/):

The *Gamma function* satisfying $\Gamma(n) = (n-1)!\quad\forall n\in\mathbb N$ is via the Euler integral

$$
\Gamma(z) = \int_0^\infty t^{z-1}e^{-t}dt\,.
$$

> You can find more information about **LaTeX** mathematical expressions [here](http://meta.math.stackexchange.com/questions/5020/mathjax-basic-tutorial-and-quick-reference).


## UML diagrams

You can render UML diagrams using [Mermaid](https://mermaidjs.github.io/). For example, this will produce a sequence diagram:

```mermaid
sequenceDiagram
Alice ->> Bob: Hello Bob, how are you?
Bob-->>John: How about you John?
Bob--x Alice: I am good thanks!
Bob-x John: I am good thanks!
Note right of John: Bob thinks a long<br/>long time, so long<br/>that the text does<br/>not fit on a row.

Bob-->Alice: Checking with John...
Alice->John: Yes... John, how are you?
```

And this will produce a flow chart:

```mermaid
graph LR
A[Square Rect] -- Link text --> B((Circle))
A --> C(Round Rect)
B --> D{Rhombus}
C --> D
```
