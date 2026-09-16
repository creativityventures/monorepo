# 5. Relai et service de transactions

Après la vérification, un relayer doit envoyer la transaction de destination. Le dépôt sépare cette responsabilité dans les agents et adaptateurs : le relayer prépare l’appel, le `TxService` le transmet au RPC et gère les tentatives, tandis que le router coordonne l’observation et l’exécution.

Le service de transactions prévoit des fournisseurs de secours et une logique de reprise. Cette résilience ne doit pas être confondue avec l’idempotence : une nouvelle tentative doit retrouver la même intention et éviter de remettre deux fois un transfert déjà exécuté.

Les intégrations Gelato et Connext apparaissent dans `packages/adapters/relayer`. Elles illustrent deux chemins d’envoi, avec des erreurs propres aux autorisations, aux réponses du séquenceur et à l’état de la transaction.

Pour analyser un incident, il faut corréler le `transferId`, le nonce, les événements source et destination, le hash de chaque tentative et l’état de finalité du domaine.

[Chapitre suivant : SDK, intégration et limites](./06-sdk-limites.md)
