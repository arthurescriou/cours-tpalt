# TPALT

Travaux pratique des alternants et techniques industriels.

TPALT est historiquement un cours seulement pour les alternants et présenté par un intervenant industriel. Il se place en fin de semestre du M2 et est donc très proche du départ pour le semestre en entreprise et plus tard (je vous le souhaite) le monde du travail. Pour cela ce cours est exclusivement dédié à l'apprentissage, la découverte ou le perfectionnement de techniques dites "industriels" mais plus exactement à des technologies utilisées par des entreprises susceptibles de vous embaucher.

Je suis Arthur Escriou, je m'occupe de TPALT cette année. Quand je ne donnes pas de cours je suis freelance en web/cloud (developpeur fullstack, frontend ou backend, parfois devops ou architecte cloud) et entrepreneur lorsque j'applique mes connaissances à mes projets personnels.

Ce que j'aimerais pour les semaines qui suivent c'est vous faire utiliser des technologies que je rencontre lors de mes missions ainsi que certaines méthode et architecture de projet (Je ne parle pas ici de méthode de gestion de projet. Concentrons nous sur la partie technique).

## Backend

La manière de faire un backend à beaucoup évoluer ces dernières années avec les technologies de conteneurisation et le cloud computing.
De plus la séparation frontend backend est devenu un pattern utilisé dans quasiment tous les projets modernes. Le backend est devenu un projet à part (de même que le frontend) et peut être une spécialité de votre profil.

Pour ce cours nous allons étudier (et implémenter) l'architecture micro service, sans trop nous attarder sur la théorie des architectures (un amphi de DAAR, fais par moi-même y est dédié). De même pour la conteneurisation.
Mais je suis toujours ouvert pour des discussions à ces sujets.

Pour les premières semaines vous allez vous initier à ce type d'architecture avec le projet suivant:

### Initiation au microservices

Le projet se sépare en 2 partie, la partie technique nécessaire à un backend et une telle architecture :

- un service d'authentification
- une API gateway (ou reverse proxy)

la partie métier, qui contient le code nécessaire au fonctionnement de notre application.
Pour ce mini projet d'initiation nous allons créer un mini réseau social.
Pour cela il nous faut

- un service stockant les informations des utilisateurs
  - ses informations personnels
  - ses posts (avec des commentaires et des réactions en emoji)
  - IMPORTANT : ce service ne stock que du texte et des liens(pour les photos de profils et images dans les posts)
- un service de stockage de photo
  - les photos peuvent être publique ou pas (une photo de profil est publique alors qu'un post pas forcément).
  - les photos appartiennent à un user
  - on peut imaginer que les photos publique sont disponible par recherche et par tag pour que tout le monde les réutilise sans avoir à réupload des photos
- un service contenant les relations entre les gens
  - amis, follow, match, etc
  - suggestion

Toutes ces fonctionnalités ne sont que pour donner un exemple plutot simple.
Il n'est pas forcément nécessaire de toutes les implémenter mais il est préférable d'avoir un projet avec un fonctionnement logique (inutile de créer un service photo si on ne peut pas l'utiliser par exemple)
Si vous avez le temps vous pouvez implémenter d'autre services :

- événements

etc...
