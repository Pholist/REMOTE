# REMOTE

TP2 : SIMULATION D'UN REMOTE

a-Git en ligne – Simulation d’un remote:

b-Création d’un dépôt remote… en local:

1-un depot distant est un repertoire distant situer la plupart du temps dans un serveur (serveurs accessibles via internet ou réseau d'entreprise).
depot local est un repertoire sur lequel nous apporterons des modifications locales, généralement ce référentiel local se trouve sur notre ordinateur.


c-Création d’une « équipe »:

2-cd Developpeur1
  git init 
4-cp /home/teris /home/.../Developpeur1
6-les fichiers de type class sont très volumineux à commiter à chaque fois,alors nous les ignorons. et nous committons le reste (fichiers txt,java..).
7-git rm -r --cached *.class
  touch gitignore
  git add gitignore
  git commit -m "gitignore"
4-cd Developpeur1
  git clone ../remote
5-git remote add origin ../remote
6-git push origin master
7-on trouver un ensemble des fichiers ajoutées dans le fichier objects (git push origin master poussera les modifications de toutes les branches locales vers les branches correspondantes à l'origine distante)
10-cd Developpeur2
   git remote add origin master
   git pull origin master
11-tous les depot pointent sur le meme commit(le dernier commit).
 
 d-Travail en équipe:
 
 4-
   a-le dernier commit appliqué dans le depot DEV1 n'est pas affiché dans la liste des commits du depot DEV2.
   b-git fetch ramène toutes les modifications, donc si nous tapons git lol les commits dev2 se synchroniseront avec les états de remote.
   c-les modifications ne sont pas appliquées sur workcopie (board.java)
   d-faut appliquer (merge) les modifications apportées de la branche de remote a la branche local.
6-git pull combine fetch et merge .

 e-gestion des conflits:

1-Les mises à jour ont été rejetées car le remote contient du travail que nous n'avons pas localement. Ceci est généralement causé par un autre dépôt poussant au même réf. nous devons d'abord intégrer les modifications à distance(git pull) avant de pousser à nouveau.

7-conflits de modifications.
message afficher => Auto-merging Board.java
                    CONFLICT (content): Merge conflict in Board.java
                    Automatic merge failed; fix conflicts and then commit the result.

solution => il faut se mettre d'accord sur un changement et appliquez-le avant de propager les changements pour éviter les conflits.

 
