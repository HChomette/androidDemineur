# androidDemineur
Mini-projet de démineur en Android

N'étant pas encore parfaitement familier avec l'architecture des projets Android Studio, je vous ai fourni la partie src, qui est il me semble suffisante. Si j'ai oublié une partie, n'hésitez surtout pas à me prévenir.

Le projet est constitué de 3 activités:
-La première est un simple écran d'instructions, avec un bouton qui emmène à l'activité suivante.

-La deuxième est un écran de choix de difficulté. On choisit entre facile, moyen ou difficile. 
Pour des raisons pratiques de test, que ce soit pour vous ou pour moi, j'ai laissé la difficulté facile à 2 cases sur 2 et une seule bombe. Les deux autres difficultés sont par contre totalement jouables

-Enfin, la dernière activité est le jeu à proprement parler. On a un plateau constitué de cellules. En appuyant sur une cellule, on a bien le comportement normal d'un démineur.
Il y a également un switch drapeau pour poser des drapeaux (représentés par un D). Ceux-ci bloquent la révélation de la case pour éviter les erreurs.
On peut également les enlever en rappuyant simplement dessus avec le switch drapeau activé.

# Choix techniques

Comme demandé, j'ai fait très simple dans les graphismes. On se contente de caractères pour afficher les bombes, drapeaux, et nombres de bombes adjacentes.
Mon plateau de jeu est constitué de Cellules, une classe que j'ai crée, dont la superclasse est simplement Button. Cela me permet d'attacher facilement un onClickListener, de changer le texte dessus, la couleur etc.
Le plateau en lui même est un TableLayout dans une ScrollView. On peut donc placer simplement les cellules, et scroll. J'ai choisi de scroll, plutôt que de trop réduire, parce que les caractères sur les boutons doivent rester lisibles.
Même si ce n'était pas demandé, il y a une traduction anglaise intégrée à l'application.
Tous les écrans sont disponibles dans les deux orientations, et la rotation en cours d'utilisation est bien prise en compte (on sauvegarde le plateau et l'état du switch pour l'activité de jeu).
J'ai rendu la classe Cellule Serializable, pour passer le tableau dans le Bundle. Il y avait peut être mieux, mais je travaillerai de toute façon cela en cours, il s'agit de mon prochain cours d'Android après la semaine de vacances.
Enfin, il y a une petite animation d'apparition en transparence sur la première activité.
