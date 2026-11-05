# Cartographie du processus de suivi

## Processus actuel (hypothèse à confirmer avec l’équipe)

1. Les contributeurs rédigent leurs rapports dans des fichiers ou messages séparés.
2. Un responsable relance les personnes en retard et récupère les documents.
3. Il consolide manuellement les informations dans un tableau de suivi.
4. Il partage le rapport consolidé et demande des corrections par échanges successifs.

### Tâches répétitives et risques

- Relances individuelles et accusés de réception répétés.
- Copie et recopie des informations entre formats.
- Versions multiples, champs manquants et consolidation tardive.
- Visibilité limitée sur l’état de réception des contributions.

## Processus cible proposé

1. Le contributeur ouvre le formulaire SharePoint et renseigne les dates de début et de fin de la période couverte.
2. Il saisit les informations d’activité et soumet le formulaire.
3. SharePoint crée un enregistrement central avec horodatage et identité du créateur.
4. Power Automate envoie un accusé de réception au contributeur et une notification au responsable configuré.
5. Le responsable suit les rapports dans la liste SharePoint et utilise ses vues filtrées pour la consolidation.

Le prototype ne met pas en place d’approbation ni de relance planifiée : ces règles doivent être confirmées avant extension.
