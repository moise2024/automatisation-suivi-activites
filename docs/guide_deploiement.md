# Guide de déploiement

1. Dans un site SharePoint de test, créer une liste personnalisée nommée **Suivi des activités**.
2. Ajouter les champs décrits dans `config/liste_sharepoint.json`. Utiliser les noms internes proposés sans accents.
3. Rendre obligatoires le titre, les dates, l’activité et le courriel. Ajouter une validation empêchant une date de fin antérieure à la date de début.
4. Créer des vues « Tous les rapports » (responsable) et « Mes rapports » (filtrée par créateur). Limiter les permissions selon les règles de l’organisation.
5. Créer un flux automatisé avec le déclencheur et les actions de `specification_flux_power_automate.md`.
6. Configurer les connexions et adresses de notification du tenant. Ne pas utiliser une adresse personnelle comme propriétaire permanent du flux.
7. Tester en environnement de test : soumission valide, champ requis manquant, période invalide, courriel incorrect et échec temporaire d’envoi.
8. Faire valider le formulaire, les destinataires et les autorisations par le responsable avant publication.

Les interfaces Microsoft évoluent : les libellés peuvent légèrement différer selon la version du tenant.
