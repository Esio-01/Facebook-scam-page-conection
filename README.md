![fake page](https://cdn.discordapp.com/attachments/633782210238873612/894714836359991327/unknown.png)
# Page de phishing pour facebook
 
## 1. Informations
Page de phishing simulant la page de connexion PayPal. 
Faite en php, elle fournit:
  - email
  - mot de  passe
  - IP
  - date/heure (à la seconde près)
  - Pays
  - Région
  - Ville
  - Code postal
  - Coordonées (latitude, longitude)
  - Fuseau horaire
  - Langues
  - ASN
  - ISP
  - Navigateur
  - User agent


### Exemple:
![example.txt](https://cdn.discordapp.com/attachments/633782210238873612/894718281028624414/unknown.png)


----
## 2. Fonctionnement générale


Les informations sont stocké dans le fichier "data.txt" après que la personne ai envoyer le formulaire en cliquant sur "Se connecter".
----
## 3. Fonctionnalité

La page est équipé:
  - d'un auto ip blacklist
  - d'un system de redirection au choix pour les ip blacklist et après la connexion
  - de logs
  - d'un system de webhook discord (pour reçevoir vos infos via un salon)
----
## 4. Fonctionnement

  ### A. L'auto ip blacklist/ip locker
  Fonctionnalitée très utile pour éviter les spam/ddos/vengeance ou autre, le principe est relativement simple, une fois que la personne à visité votre fausse page de connexion (plus précisément: une fois que la personne à envoyer son formulaire de connexion "PayPal"), son ip va s'inscrire dans un fichier nommé "blacklist.txt". Vous l'aurez compris, une fois votre ip sur ce fichier il n'est plus possible d'accéder au site. A la place, la personne seras redirigé sur une page (plus d'info au paragraphe B ). Vous verrrez dans le fichier "blacklist.txt" qu'il y as déjà 11 810 IP inscrit. Ces ip sont connu pour le ddos etc... J'ai donc pris les soins de les mettre par défaut pour diminuer les chance aux personnes qui tentent d'attaquer votre page de connexion.

### B. Redirection des ip blacklist et après la redirection, au choix.
Comme vous l'avez vu dans le paragraphe précédent, les ip inscrit dans le fichier "blacklist.txt" ne peuvent accéder au site. Tout les utilisateurs venant sur le site avec une ip figurant sur le fichier "blacklist.txt" seront donc redirigé vers une page au choix (défini par vous aupréalable). Pour définir la page de redirection, il vous suffit d'ouvrir le fichier redirection_blacklist.txt et de mettre l'url de votre choix à la place de "YOUR URL REDIRECTION !". Une fois enregistré, les modifications seront appliqué.
Il en va de même pour la redirection après la connexion de l'utilisateur sur votre page, il seras redirigé vers le site spécifié dans le fichier "redirection.txt".
Conseil: Il est préférable de rediriger votre cible sur une page de recherche facebook, il auras alors une impression de bien s'être connecté sur son compte.

  ### C. Les logs
   Simple d'accès, il vous suffit d'ouvrir le fichier "logs.txt". Toutes les visites sur votre page seront stocké dans ce fichier avec pour infos sur chaque visites:
 - IP
 - date/heure à laquel ils ont visité votre page

   Les logs vous préciserons si la personne est déjà venu sur votre site auparavant, et si oui, les logs préciserons la redirection de l'utilisateur (le lien spécifié      dans le fichier "redirection.txt").
   
### D. Webhook Discord
Possibilité de lié un webhook discord à votre scam page ! Aussi simple d'utilisation que toute les autres fonctionnalitées. Il vous suffit d'ouvrir le fichier "discord_webhook.txt" et de remplacé votre webhook à la place de "YOUR WEBHOOK URL HERE". Une fois cela fait et enregistré, les modifications seront appliqué et les formulaires de connexion de votre page seront renseigné non seulement sur le fichier "data.txt", mais aussi sur le salon qu'occupe votre webhook sous cette forme:

![webhook.txt](https://media.discordapp.net/attachments/633782210238873612/882065636883312670/unknown.png?width=597&height=630)

Si vous avez des soucis à propos de cette scam page, vous pouvez me contacter sur discord:
  - Pseudo: Esio#4871
  - Serveur: https://discord.gg/WXZAHr3HP6

----

