# 1. Connext : le rôle du protocole

Connext est une pile de communication généralisée entre blockchains. Elle permet à une application de demander un transfert d’actif ou un appel distant sans imposer un pont unique à tous les cas d’usage.

Le dépôt sépare les contrats déployés, les services d’exécution, les routeurs, le SDK, les adaptateurs et les utilitaires. Le README décrit cinq couches : application, liquidité, exécution, vérification et transport.

Le modèle est optimiste et opérationnel : des routeurs fournissent rapidement la liquidité, tandis que des services observent les événements et font progresser le message. Cette séparation rend le système composable, mais elle déplace une partie de la confiance vers les paramètres, les watchers et les relayeurs.

Ce parcours suit d’abord l’appel cross-chain, puis la liquidité et la vérification.

[Chapitre suivant : xcall et cycle de transfert](./02-xcall-cycle.md)
