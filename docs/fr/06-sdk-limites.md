# 6. SDK, intégration et limites

Le SDK fournit une façade JavaScript autour des appels de contrats et des données de transfert. Les exemples sous `packages/examples` montrent comment une application peut sélectionner un actif, construire un appel et suivre son identifiant sans connaître tous les détails des agents internes.

Une intégration sérieuse doit valider les domaines autorisés, l’actif canonique, le destinataire, les données d’appel, le slippage, le delegate et la politique de reprise. Elle doit aussi afficher à l’utilisateur la différence entre demande créée, liquidité fournie, message vérifié et exécution finale.

Ce parcours ne constitue ni un audit ni une garantie de disponibilité. Les risques incluent la dépendance aux routeurs et watchers, les erreurs d’indexation, les retards de finalité, les changements d’AMB, la gestion des clés de service et les appels destinataires non sûrs.

Périmètre : lecture statique du code et du README du dépôt amont, sans nouvelle installation, compilation, exécution de tests ni déploiement. Les vérifications reproductibles sont décrites dans la suite de tests du dépôt pour les lecteurs qui souhaitent les exécuter séparément.

[Retour au sommaire](./README.md)
