# Exercice 2. Prise en main de l’interpréteur de commandes
## Manuel

1)
La commande `which` permet de donner le chemin d'acces au fichier executé lors de l'execution d'une commande.

exemple : `which ping`

donnera en sortit : `/usr/bin/ping`

2)
on peut chercher un terme particulier dans le manuelle en ecivant `/` suivie de l'expression ou l'expression régulière recherché,la touche `N` peut etre ensuite utilisé pour aller a l'itération suivante de l'expression.

3)
On quitte le manuele en appyuyant sur la touche `Q`.

4)
man 6 man
// TODO //

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

la commande `time` suivit d'une commande permet d'optenir le temps d'execution de cette commande.

2)
les fichiers commençant par un point sont des fichier cacher.

3)


# Exercice 3. Découverte de l’éditeur de texte nano

# Exercice 4. Personnalisation du shell

# Exercice 5. Pour les plus rapides
