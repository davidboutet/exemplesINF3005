Courriels et authentification
=============================

Les applications web utilisent souvent le courriel pour communiquer avec ses
utilisateurs. Notamment, le processus d'authentification implique généralement
une communication par courriel afin de valider l'adresse courriel de
l'utilisateur et pour la procédure de recouvrement en cas de perte de mot de
passe.

Objectifs
---------

* Envoyer des courriels
* Manipuler l'authentification dans une application web

Exercices
---------

1. Créez un compte [https://www.google.com/gmail/](Gmail) spécifiquement pour le
   cours INF3005.

2. À l'aide de cet [https://github.com/jacquesberger/exemplesINF3005/blob/master/email/gmail.py](exemple),
   envoyez un courriel à partir de l'adresse créée à l'exercice précédent.

3. Faites une copie de l'[https://github.com/jacquesberger/exemplesINF3005/tree/master/Flask/login](exemple de _login_) vu en classe
   et modifiez-le pour saisir le nom et le prénom de l'utilisateur lors de son
   inscription. Ensuite, lorsque l'utilisation est connecté à l'application,
   affichez-lui une salutation avec son nom complet sur la page d'accueil.

4. Mettez en place une procédure de validation d'adresse courriel lors de
   l'inscription d'un nouvel utilisateur. Utilisez la technique présentée en
   classe, c'est-à-dire :
   * l'utilisateur s'inscrit sur le site;
   * le site génère un jeton unique et aléatoire pour l'utilisateur;
   * le site envoie un courriel à l'utilisateur avec lien pour valider son
     adresse courriel (exemple :
     `http://localhost:5000/activation/<jeton>`);
   * l'utilisateur clique sur le lien.

   Si l'utilisateur n'a pas validé son adresse courriel, un message apparaît
   pour l'aviser sur la page d'accueil (note : ajoutez un booléen dans la BD
   pour indiquer si l'adresse a été validée ou non).
