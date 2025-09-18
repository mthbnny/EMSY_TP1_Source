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

Qwerty

Q2. disposition du clavier suisse-romand ?

Qwertz

Q3. disposition du le clavier français ? 

Azerty


H. Déplacez-vous à la **racine du système** en utilisant la commande suivante : `cd` 

> vore commande ?!

I. Affichez le contenu de la racine avec la commande : `ls –l`	

![Virtual disk](/Images/ls-s.png) 

Q5. Que signifie l'option `-l` avec la commande `ls` 

Qwerty

Q6. Décrypter la ligne où se trouve le répertoire **home**    

[Placer votre capture d'écran]()

Qwertz

J. Créez un répertoire de travail nommé « EMSY_VosInitiales» dans quel dossier racine allez-vous le placer (justifiez votre réponse) et quelle commande allez-vous utiliser. 



Q7. Si vous créez un répertoire de travail (pour éditer/sauvegarder des fichiers), dans quelle **répertoire racine** vous vous placez ? 

> ça affiche la liste longue


K. Dans ce répertoire, créez un fichier texte que vous nommerez `TESTSLO_XXX_XXX` et éditez celui en écrivant un texte, exemple : "TP linux by XXX et XXX".
	Utiliser la commande `vi`

> votre commande ?! 

Q9. dans le répertoire `/home`, pouvez-vous éditez un fichier uniquement avec la commande `vi` 

> votre réponse ?!

Q10. Si vous éteignez la machine virtuelle et que vous la rallumez, est-ce que le répertoire créé ci-dessus existe toujours (justifiez votre réponse) ? 

> votre réponse ?!

L. Tapez la commande `ls -l /dev/sda` 

![Placer votre capture d'écran]() 

Q11. Que signifie **sda** ? 

> votre réponse ?!

Q12. Décrypter la réponse après avoir taper la commande `ls -l /dev/sda` -> voir résultat point 13.

> votre réponse ?!


## Tips 

> $$Tips^1$$ : sortir de la VM -> appuyer simultanément sur `Ctrl` et `Alt` 

> $$Tips^2$$ : arrêter la VM proprement -> commande : `shutdown`

> $$Tips^3$$ : arrêter la VM pour cause de plantage -> commande : `halt` ou `poweroff`

> $$Tips^4$$ : [commande vi avec ses options](https://www.linuxtricks.fr/wiki/guide-de-sur-vi-utilisation-de-vi)

> $$Tips^5$$ : [éditer un fichier type markdown (.md)](https://ashki23.github.io/markdown-latex.html)

