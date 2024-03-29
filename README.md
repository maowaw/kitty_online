	Voici l'ordre des lignes de commandes à connaître pour manipuler les branches :


$ git checkout master : pour s'assurer qu'on est bien sur la branche master sur son ordi.

$ git pull origin master : pour récupérer de GitHub la dernière version de master.

$ git branch nom_de_ta_feature : pour créer une branche nommée "nom_de_ta_feature" à partir de master qui est désormais à jour.

$ git checkout nom_de_ta_feature : pour se positionner sur la branche "nom_de_ta_feature".
à partir de là, on se met à coder normalement. Chaque commit aura lieu uniquement sur la branche "nom_de_ta_feature". Pour cela, on utilise les classiques :

$ git add . pour préparer à commit tous les fichiers ayant été modifiés

$ git commit -m "commentaire sur mon commit" pour faire un commit



	Pour fusionner la branche contenant ton travail, voici la marche à suivre, étape par étape :

$ git checkout master : tu te remets sur la branche master en vue de la mettre à jour (ça fait 3 jours que tu ne l'as pas fait) ;

$ git pull origin master : tu récupères de GitHub tout le travail qui a été effectué et mets la branche master à jour ;

$ git checkout nom_de_ta_feature : tu te remets sur ta branche de feature en vue de la fusionner ;

$ git merge master : cette commande demande à Git de fusionner master dans ta branche. L'ordre est important : c'est master qui va DANS ta branche et pas l'inverse. La branche master n'est pas modifiée pour le moment.
optionnel : gestion de conflits (voir plus loin)

$ git checkout master : tu te remets sur master

$ git merge nom_de_ta_feature : cette fois, on fait la fusion dans l'autre sens. On fusionne ta branche DANS master. La branche master est donc mise à jour.
optionnel : gestion de conflits (voir plus loin)

$ git push origin master : Maintenant que la fusion est faite, il faut mettre GitHub à jour pour que tous tes collègues aient l'info. Donc envoie la branche à jour sur Github 🙌