# DYONISOS 🍷

Cave à vin virtuelle en 3D : on choisit le nombre de rangées et de colonnes de son casier, on voit les culs des bouteilles, et un toucher sort la bouteille avec tout ce qu'il faut savoir pour bien la déguster.

## Fonctionnalités

- **Cave 3D paramétrable** : jusqu'à 20 rangées × 30 colonnes, repérage A1, B4…
- **Bouteilles réalistes** : formes Bordeaux, Bourgogne, Alsace (flûte) et Champagne selon la région et le type.
- **Sortie animée** : la bouteille glisse hors du casier, se redresse et affiche son étiquette.
- **Fiche de dégustation** :
  - statut de maturité (trop jeune, prêt, apogée, à boire vite, déclin) et frise de la fenêtre de dégustation ;
  - température de service et délai pour sortir la bouteille de la cave ou la rafraîchir ;
  - aération / carafe selon l'âge, verre conseillé, accords mets-vin, conservation.
- **Photo d'étiquette** : on photographie l'étiquette, l'IA la lit et remplit toute la fiche (cuvée, domaine, appellation, région, type, millésime, cépages + avis sommelier). La photo devient l'étiquette de la bouteille en 3D.
- **Mode Maturité** : un anneau coloré sur chaque cul de bouteille.
- **Inventaire** trié par urgence, recherche, historique des bouteilles dégustées.
- **Sauvegarde** : export/import JSON depuis le menu ⚙.

## Utilisation

Un seul fichier : `index.html` (Three.js chargé depuis cdnjs).

- **En local** : ouvrir `index.html` dans un navigateur. Les données sont gardées dans le navigateur (localStorage).
- **GitHub Pages** : Settings → Pages → Source « Deploy from a branch » → `main` / `root`. L'app sera en ligne sur `https://erochel.github.io/Dyonisos/`.
- **Sur claude.ai** : la version publiée en artifact synchronise la cave dans le compte et ajoute le « Sommelier IA ».

## IA (lecture d'étiquette & sommelier)

- Sur claude.ai : fonctionne directement.
- Sur GitHub Pages : ⚙ → *Intelligence artificielle* → coller une clé API Anthropic. Elle reste dans le navigateur de l'appareil, l'usage est facturé sur le compte Anthropic.

## Modèle de garde

Les températures, conseils d'aération et fenêtres de dégustation de base viennent de règles générales de sommellerie codées dans l'app (9 familles de vins, coefficient de garde par région, âge du vin). Ce sont des estimations moyennes, pas des données propres à chaque cuvée. Elles peuvent être remplacées par vos propres années (« À boire dès / Jusqu'à ») ou par l'avis du sommelier IA.
