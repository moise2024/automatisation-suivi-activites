# Spécification du flux Power Automate

## Flux : notification à la soumission

1. **Déclencheur** : SharePoint — lorsqu’un élément est créé, sur le site et la liste « Suivi des activités ».
2. **Vérification** : s’assurer que le courriel du soumetteur est renseigné et que la période est cohérente. Le formulaire doit déjà imposer les champs requis.
3. **Accusé au soumetteur** : envoyer un courriel à `CourrielSoumetteur` avec le titre du rapport, la période, la date de création et un lien vers l’élément.
4. **Notification au responsable** : envoyer un courriel à la variable de configuration `RESPONSABLE_SUIVI_EMAIL`, avec le contributeur, la période, le titre et le lien vers l’élément.
5. **Erreur** : configurer les deux envois dans une portée distincte. En cas d’échec, consigner l’erreur dans l’historique d’exécution et notifier l’administrateur du flux si l’adresse `ADMIN_FLUX_EMAIL` est configurée.

## Paramètres à fournir dans le tenant

- URL du site SharePoint et nom interne de la liste.
- Connexion du compte de service ou propriétaire du flux.
- `RESPONSABLE_SUIVI_EMAIL` et `ADMIN_FLUX_EMAIL`.
- Modèle de sujet : `Rapport reçu — [Titre du rapport]`.

Ne pas inclure de données personnelles sensibles dans le courriel. Le message doit pointer vers l’élément SharePoint, où les autorisations s’appliquent. Tester les droits d’accès du soumetteur et du responsable avant mise en service.
