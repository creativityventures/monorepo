# 3. Routeurs, liquidité et séquenceur

Les routeurs sont les fournisseurs de liquidité du parcours rapide. Ils observent les demandes, évaluent le montant et le slippage, puis soumettent une proposition. Le séquenceur agrège ces offres et publie la réponse qui permet de démarrer l’exécution.

Le code de `packages/agents/router` distingue l’écoute, la construction de l’exécution et les contrôles : version compatible, routeur autorisé, réponse du séquenceur valide et signatures cohérentes. Une offre n’est donc pas seulement un prix ; elle est aussi une autorisation d’agir dans un contexte précis.

La liquidité accélère l’expérience utilisateur, mais elle introduit une obligation de réconciliation : le routeur doit être remboursé ou recevoir le règlement prévu lorsque le message est confirmé. Les actifs, domaines, montants et délais doivent rester liés au même identifiant de transfert.

Les scénarios de panne à documenter sont le manque de liquidité, l’expiration d’une réponse, la double soumission et l’écart entre un événement observé et l’état réellement finalisé.

[Chapitre suivant : transport, AMB et vérification](./04-transport-verification.md)
