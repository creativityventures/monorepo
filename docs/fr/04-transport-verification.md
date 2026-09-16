# 4. Transport, AMB et vérification

Connext ne dépend pas d’un seul transport. Les adaptateurs AMB encapsulent les mécanismes de messagerie disponibles entre domaines, tandis que le watcher vérifie les événements et les racines avant de laisser progresser le règlement.

La couche de transport fournit le message ; la couche de vérification vérifie que le message correspond à une séquence et à une preuve attendues. Dans `packages/adapters/watcher`, les vérificateurs traitent notamment les racines et les actifs. Cette séparation évite de confondre « message relayé » et « transfert prouvé ».

Une racine Merkle compresse un ensemble d’événements. Sa sécurité dépend de la construction de l’arbre, du chemin fourni, du domaine concerné et de l’absence de réutilisation sur un autre contexte. Les données d’indexation servent à retrouver les éléments, mais ne remplacent pas la vérification cryptographique.

Les limites importantes sont la disponibilité des watchers, la fraîcheur des données, les changements de configuration AMB et les différences de finalité entre chaînes.

[Chapitre suivant : relai et service de transactions](./05-relai-execution.md)
