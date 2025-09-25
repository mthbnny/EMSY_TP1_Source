# TP1 - Installation Linux sur une VM - V0.1

## Groupe 

- Luc Derré - Bonny Mathéo

## But 

Cette manipulation a pour but d'installer une distribution linux [Sparky Linux](https://sparkylinux.org/) dans une machine virtuelle VMware Workstation Player, à l’aide d’une image disque (ISO).

## Materiels à disposition 

- VMware Workstation Player - V17
- Image disque (ISO) : sparkylinux-6.4-x86_64-minimalcli.iso

## Utilisation de VMware et de l'image ISO linux 

A. Lancez VMware Workstation Player (logiciel)  

B. Sélectionnez **Create a New Virtual Machine** 

C. Placez le fichier `.iso` dans une repertoire connu : 

`C:\VosInitiales\VM\ISO`

D. Indiquez le chemin d’accès de l’image iso comme indiqué sous l’image ci-dessous :

![install image disk](/Images/Install_ISO.jpg) 

E. Choisir un nom d'OS : `Linux - Debian 11.x` 

![OS name choice](/Images/OS_Choice.jpg) 

F. Nommez la machine virtuelle : `SparkyLinux-VosInitiales` 

G. Creez un disque virtuel -> capcité : **20GB** 

> remarque$$^1$$ : cocher **store virtual disk a single file**

![Virtual disk](/Images/VirtualDisk.jpg) 

> remarque$$^2$$ : ci-dessous, la configuration de la VM 

![Virtual disk](/Images/VM_Config.jpg) 

H. Lancez la machine virtuelle : **Play virtual machine** 

## Lancement de l'image ISO (Linux - Live CD) 

G. Lancement du live CD : 

![Virtual disk](/Images/Linux-dep1.png) 

Shell Linux : 

![Virtual disk](/Images/linux-shell.png) 

> **ATTENTION** : par défaut, le clavier est configuré est **Clavier Americain**

Q1. disposition du clavier américain ?

>Qwerty

Q2. disposition du clavier suisse-romand ?

>Qwertz

Q3. disposition du le clavier français ? 

>Azerty


H. Déplacez-vous à la **racine du système** en utilisant la commande suivante : `cd` 


I. Affichez le contenu de la racine avec la commande : `ls –l`	

![Virtual disk](/Images/ls-l.png) 

Q5. Que signifie l'option `-l` avec la commande `ls` 

>ça liste les fichiers du système
>et le `-l` liste les options du fichier

Q6. Décrypter la ligne où se trouve le répertoire **home**    
![Virtual disk](/Images/home.png) 

>drwxr-xr-x:(d)indique un répertoire (rwx) qui correspond aux permissions du propriétaire, le r pour le read du contenu, le w pour write pour ^tre capable d'ajouter/enlever des fichiers et sous répertoir, x pour accès au contenu du répertoire et aux fichiers qu'il contient. r-x correspond au droit pour le groupe et x autorise l'accès au répertoire, - indique qu'il n'y a pas de permission d'écrire par le groupe et x autorise l'accès au répertoire. le deuxième r-x correspond aux droit pour les autres utilisateurs. 1 root root indique le nombre de personnes liées au dossier. Le premier root indique l'utilisateur qui possède le répertoire et le deuxième indique le groupe auquel appartient au répertoire. Le nombre 60 correspond a l'espace utilisé en octet. Enfin la date est indiquée en format (mois/jours/heure).

J. Créez un répertoire de travail nommé « EMSY_VosInitiales» dans quel dossier racine allez-vous le placer (justifiez votre réponse) et quelle commande allez-vous utiliser. 

>dans le répertoire home car c'est un répertoire personnel
>
>.cd home `mkdir EMSY_MBY`


Q7. Si vous créez un répertoire de travail (pour éditer/sauvegarder des fichiers), dans quelle **répertoire racine** vous vous placez ? 

> home


K. Dans ce répertoire, créez un fichier texte que vous nommerez `TESTSLO_XXX_XXX` et éditez celui en écrivant un texte, exemple : "TP linux by XXX et XXX".
	Utiliser la commande `vi`

> `vi TESTSLO_LDE_MBY`

Q9. dans le répertoire `/home`, pouvez-vous éditez un fichier uniquement avec la commande `vi` 

> oui

Q10. Si vous éteignez la machine virtuelle et que vous la rallumez, est-ce que le répertoire créé ci-dessus existe toujours (justifiez votre réponse) ? 

> Oui car éteindre  et allumer ne supprime pas les fichiers stockés sur le disque virtuel, et les dossiers dans le home sont écrits sur ce disque virtuel

L. Tapez la commande `ls -l /dev/sda` 

![Placer votre capture d'écran]() 

Q11. Que signifie **sda** ? 

> SDA signifie que c'est le premier disque dur SCSI le disque dur principal(small Computer system Interface)

Q12. Décrypter la réponse après avoir taper la commande `ls -l /dev/sda` -> voir résultat point 13.

> votre réponse ?!


Q14. A quoi sert la partition swap ? Est-ce que ce principe existe sur les OS Microsoft Windows ?

Q15. Quel format pourriez-vous utiliser pour la 3ème partition afin qu’elle soit également accessible depuis un OS Microsoft ?

Q16. Durant l’installation, on vous demande deux noms d’utilisateur. A quoi correspondent-ils ?

N. Après l’installation de Linux, prenez une capture d’écran du démarrage de votre système (GRUB).

O.Trouvez la ou les lignes de commande permettant de changer le clavier (clavier suisse romand trouvable sous « German (Switzerland)) et procédez à la configuration du clavier.

P.Testez si l’application « nano » est installée sur votre machine, tapez la commande :
nano -version

Q17. À quoi sert « nano » ?

Q.Testez si l’application « git » est installée sur votre distribution, si ce n’est pas le cas installez un client git.

Q18. Comment savoir si « git » est déjà installé ?

Q19. Quelle(s) commande(s) utilisez-vous pour l’installer ?

Q20. Que veut dire « apt » ?

Q21. Est-ce que cette commande peut être utilisée sur toutes les distributions Linux ?

LABO EMSY ETML-ES

PBY/NMI/SCA EMSY01 TP1A - InstVMLinux_v2_6.docx 5/5
R.Créez un sous-répertoire « EMSY_TP1_XXX-YYY » dans le répertoire de votre utilisateur. Attention : Ici on veut que l’utilisateur (vous) ait les droits de lecture, d’écriture et d’exécution. Q22. Quel est le répertoire utilisateur ?

Q23. Quelles sont les commandes que vous allez utiliser ?

S.Dans ce répertoire, tapez la commande :
git clone https://github.com/votreDepot/EMSY_TP1_Source

Il faut au préalable que vous ayez mis en place à cette adresse un fork du dépôt fourni.

Q24. Qu’observez-vous dans votre répertoire ?

T.Editez le fichier source .c avec l’éditeur de texte « nano ».
Réalisez un petit programme en C (par exemple de type « Hello world »).

U.Vérifiez si le compilateur « gcc » est bien installé.

Notez la version du logiciel.

Tapez les commandes suivantes :

gcc -Wall -o fichier.o -c fichier.c

gcc -o fichier fichier.o

Remarque : « fichier » est à remplacer par le nom de votre choix

Q25. Quels sont les fichiers qui ont été générés ?

V.Entrez la commande suivante :./fichier

Q26. Que se passe-t-il ?

## Tips 

> $$Tips^1$$ : sortir de la VM -> appuyer simultanément sur `Ctrl` et `Alt` 

> $$Tips^2$$ : arrêter la VM proprement -> commande : `shutdown`

> $$Tips^3$$ : arrêter la VM pour cause de plantage -> commande : `halt` ou `poweroff`

> $$Tips^4$$ : [commande vi avec ses options](https://www.linuxtricks.fr/wiki/guide-de-sur-vi-utilisation-de-vi)

> $$Tips^5$$ : [éditer un fichier type markdown (.md)](https://ashki23.github.io/markdown-latex.html)

