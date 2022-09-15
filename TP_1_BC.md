
# Exercice 2. Prise en main de l’interpréteur de commandes
## Manuel

1)
La commande `which` permet de donner le chemin d'acces au fichier executé lors de l'execution d'une commande.

exemple : `which ping`

donnera en sortit : `/usr/bin/ping`

2)
on peut chercher un terme particulier dans le manuelle en ecivant `/` suivie de l'expression ou l'expression régulière recherché,la touche 'N' peut etre ensuite utilisé pour aller a l'itération suivante de l'expression.

3)
On quitte le manuele en appyuyant sur la touche 'Q'.

4)
`man 6 man` ne trouve pas de 6eme section.

## Navigation dans l’arborescence des fichiers
1)
On utilise la commande `cd /var/log` pour allez dans le dossier /var/log.

2)
On utilise la commande `cd ..` pour allez dans le dossier /var depuis le dossier /var/log.

3)
On retourne dans le dossier personnel avec la commande `cd /` ou `cd`.

4)
On retourne dans le dossier /var grace a la commande `cd -`.

5)
Lorsque l'on essaye de se rendre dans le répertoire /root avec la commande `cd /root`.

Une erreur bash apparait :

`-bash: cd: /root: Permission denied`

Cette erreur indique qu'on ne posséde pas les permission d'accéder a ce dossier.

6)
La commande `sudo cd /root` affiche une erreur :

`sudo: cd:command not found`

Cette erreur indique que la commande `cd` n'est pas trouver.

Car `cd` est une commande qui interne a bash et n'est pas 'executable'.



Pour pouvoir utilisé `cd` en root ils faut d'abord se logger en root avec `sudo su`.
ensuite on peut la commande `cd /root` on peut accedé au dossier /root.

7)
On crée l'arborescense grace aux commandes `mkdir` et `touch` :

exemple : 

`mkdir Dossier1` pour crée le dossier `Dossier1` a partir du répertoire courant.

`touch Dossier1/Fichier1` pour crée le fichier `Fichier1` dans `Dossier1`.

8)
on utilise la commande `rm Dossier1/Fichier1` pour supprimer le `Fichier1`.

Puis on utilise `rm -d Dossier1` pour supprimer le `Dossier1` (l'option -d permet de supprimer des dossier).

9)
La commande `rm -d [dossier]` permet de supprimer des dossier.

10)
Ce n'est pas possible de supprimé le `Dossier2` car il n'est pas vide.

11)
La commande `rm -r Dossier2` permet de supprimer le `Dossier2` et son contenue.

## Commandes importantes

1)
La commande `date` permet d'afficher l'heure.

la commande `time` suivit d'une commande permet d'obtenir le temps d'exécution de cette commande.

2)
les fichiers commençant par un point sont des fichier cacher.

3)
le programme `ls` se trouve dans le répertoire `/usr/bin/ls`.

4)
Il n'existe pas de manuel pour la commande `ll` ,cette commande correspond a la commande `ls -alF`.

On le sait grâce a la commande `alias ll`.

5)
la commande `ls /bin` permet d'(afficher le contenue de `/bin`.

6)
la commande `ls` affiche le contenue du répertoire courant.

7)
la commande `pwd` qui donne le chemin complet du dossier courant.

8)
la commande `echo 'bip' > plop` exécuté 2 fois écrit "bip" dans le fichier `plop` (du répertoire courant).

9)
la commande `echo 'bip' >> plop` exécuté 2 fois écrit "bip bip" dans le fichier `plop` (du répertoire courant).

10)
la commande `sleep 10 | echo 'toto'` va attendre 10 seconde et afficher "toto" en même temps.

11)
la commande `file` indique le type du fichier indiqué par la commande ainsi que la norme de caractère utilisé dans ce fichier.

12)
la commande `ln original lien_phy` permet de lien le contenue du fichier `original` au fichier `lien_phy`.

Si `original` est supprimé, alors `lien_phy` garde le contenu du fichier `original` avant sa suppression.

13)
la commande `ln -s lien_phy lien_sym` crée un lien symbolique.

Lors de la modification de `lien_phy` ou de `lien_sym` le contenue de l'autre fichier ne change pas.

Lors de la suppression de `lien_phy` ,le contenue du fichier `lien_sym` ce supprime.

14)
On utilise 'CTRL + S' pour interrompre le défilement d’un résultat  et  'CTRL + Q' pour reprendre le défilement.

15)
la commande `head -5 /var/log/syslog` affiche les 5 première ligne du fichier `syslog`.

la commande `head -n -15` affiche les 15 dernière ligne du fichier `syslog`.

la commande `sed -n '10,20p' filename` affiche les ligne 10 a 20 du fichier `syslog`.

16)
la commande `dmesg` permet les processus de démarrage Linux. 

`less` permet de ne pas tout faire défiler d'un cout.

17)
le fichier `/etc/passwd` contient les mots de passe sur le systèmes.

la commande `passwd` permettant à un utilisateur de changer son Mot de passe. 

18)
on affiche la première colonne triée par ordre alphabétique inverse avec la commande :
`awk 'FS=":" {print $1}' /etc/passwd | sort -r`.

19)
la commande `wc -l /etc/passwd` affiche le nombre d'utilisateur.

20)
la commande `man -K conversion | grep 'conversion' | wc -l` affiche le nombre pages de manuel comportent le mot-clé conversion dans leur description.

21)
la commande `find / -name passwd` affiche le nom de tous les fichier se nommant `passwd` présents sur la machine.

22)
on utilise la commande la commande `find / -name passwd > ~/list_passwd_files.txt 2> /dev/null` pour que la liste des fichiers trouvés soit enregistrée dans le fichier `~/list_passwd_files.txt` et que les erreurs soient redirigées vers le fichier spécial `/dev/null`.

23)
grep ll ne fonctionne pas.
on ne peut pas trouver cette information avec grep.

24)
On utilise la commande `locate history.log` pour trouver le fichier history.log.

25)
Si on cherche un fichier que l'on vient de crée dans notre dossier personnel il n'est pas trouver par `locate`.

cela arrive car `locate` va chercher les fichier dans une base de donnée (pour être plus rapide) contrairement a la commande `find` qui cherche dans l'arborescence.

# Exercice 3. Découverte de l’éditeur de texte nano
1)
On utilise la commande `cp /var/log/syslog log.txt` pour copier `syslog` dans notre dossier personnel.

2)
On fait 'ALT + R' sur le clavier ,on indique l'occurrence a remplacé `kernel` puis le remplacement ici `noyau`.
On appuie ensuite sur 'A' pour tout remplacé.

3)
On fait 'ALT + A' pour sélectionner les 10 première ligne du fichier ,on fait 'CTRL + K' pour 'couper' puis 'CTRL + U' pour coller a la fin du fichier.

4) 
On peut faire 2 fois ALT + U pour annuler cette action.

5)
Pour quitter en enregistrant le fichier on fait 'CTRL + X' puis 'Y' pour sauvegarder puis 'ENTER' pour validé le nom.

# Exercice 4. Personnalisation du shell
1)
on utilise la commande `cp .bashrc .bashrc_bak` pour copier `.bashrc`.

2. et 3.

l'invite de commande devient vert.

4)
Pour mettre l'affichage demandé il faut mettre :
`\033[01;91m\] [\d] \033[00m\] -`
devant le `\[\033[1;32m]\u@\h\[\033[00m\]` sur la ligne de `PS1`.
