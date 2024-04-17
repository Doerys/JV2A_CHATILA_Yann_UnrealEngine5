# JV2A_CHATILA_Yann_UnrealEngine5
 
Dans mon projet, j'ai des picks up objects qui augmentent la vie du personnage affichée dans l'UI (symbole de coeur et texte).
L'UI est simple, et ancrée en haut à droite du canvas.

S'il tombe dans un gouffre, il meurt, et ça recharge la scène (détecte la localisation en axe Z du joueur). Même chose s'il tombe à 0 PV, via une variable
int de score qui augmente ou décroît au fur et à mesure des événements.

Des pièges (pics) lui font perdre un PV au contact et sont détruits au contact.

Les IA étaient supposés avoir la même logique que les pics (perte de PV et autodestruction au contact), mais n'ont pas l'air de fonctionner complètement, 
jusqu'à maintenant. Cependant, les IA sont en mesure de se déplacer vers le joueur lorsqu'il est suffisamment proche.

Je pense avoir compris pourquoi : dans la "Task" custom d'attaque j'ai créé, d'après mon code, c'était l'IA Controller qui est détruit, plutôt que l'IA Character.
Il faut donc que je trouve un moyen de faire en sorte de récupérer l'IA Character. Mais impossible de trouver comment le "récupérer" pour le détruire. Dommage, 
il ne me manquait plus que ça !