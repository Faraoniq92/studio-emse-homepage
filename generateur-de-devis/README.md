# Programme de Mission — Studio Emsé

Checklist interactive pour les missions d'architecture d'intérieur.

## Fonctionnalités

- **9 phases** de mission (Prise de contact → Chantier) avec toutes les prestations
- **3 colonnes de cases à cocher** : Architecte, Maître d'Ouvrage, Missions Complémentaires
- **Récapitulatif** filtré avec uniquement les prestations cochées
- **Prix par ligne** : affiché par défaut, retirable individuellement via ×
- **Sous-totaux par section** + Total HT calculés en temps réel
- **Export PDF** via impression navigateur (Ctrl+P → Enregistrer en PDF)

## Déploiement

Fichier unique `index.html`, aucune dépendance à installer.

### GitHub Pages

1. Push ce repo
2. Settings → Pages → Source : `main` / `/ (root)`
3. Le site sera disponible sur `https://<username>.github.io/programme-mission/`

### Autre hébergement

Copier `index.html` sur n'importe quel serveur web ou ouvrir directement dans un navigateur.

## Stack

- HTML / CSS / JS vanilla (zéro dépendance)
- Manrope (Google Fonts)
- Design system Studio Emsé
