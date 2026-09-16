# 2. xcall et cycle de transfert

L’interface de Connext expose notamment `xcall` et `xcallIntoLocal`. Une demande indique la destination, le contrat cible, l’actif, le delegate, le montant, la tolérance de slippage et les données d’appel. Le résultat est identifié par un `transferId`.

À l’origine, le contrat verrouille ou prépare l’actif et émet les informations nécessaires. Les routeurs proposent ensuite une exécution rapide sur la chaîne de destination. Le message final contient l’origine, la destination, le montant normalisé, le nonce, l’expéditeur et les données à remettre au destinataire.

Le delegate est une protection opérationnelle : il peut récupérer ou traiter un transfert qui ne peut pas être livré automatiquement. La limite de slippage borne le montant accepté, mais ne supprime ni la volatilité ni le risque d’un mauvais paramétrage de l’application.

Les types et l’ABI de `IConnext` dans `packages/agents/sdk-wrapper` donnent les points d’entrée à suivre.

[Chapitre suivant : routeurs, liquidité et séquenceur](./03-routeurs-liquidite.md)
