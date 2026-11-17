# Clés publiques de sceau d'Aplomia

Chaque photographie scellée par Aplomia porte une chaîne de vérification signée par l'une de ces clés (Ed25519). Le procès-verbal d'intégrité imprime la chaîne, la signature et l'identifiant de la clé.

## Vérifier une signature

1. Comparer la clé publique imprimée dans le dossier de preuve avec celle de `cles-sceau-publiques.txt`, pour le même identifiant.
2. Vérifier la signature en suivant les instructions du lisez-moi joint à chaque dossier de preuve.

## Les statuts

- `active` : la clé signe aujourd'hui.
- `retiree` : la clé ne signe plus, mais elle reste valable pour les signatures qu'elle a déjà posées.
- `revoquee` : la clé ne prouve plus rien à elle seule.

## Ce que ce dépôt ne contient pas

Aucun code, aucune donnée, aucun secret. Les clés publiées ici sont des clés **publiques** : la clé privée correspondante n'a jamais été écrite dans un fichier.

L'empreinte d'une clé se recalcule depuis sa forme DER : `openssl dgst -sha256 cle.der`.
