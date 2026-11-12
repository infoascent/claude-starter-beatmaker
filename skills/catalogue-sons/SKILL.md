---
name: catalogue-sons
description: Répertorie les prods, loops, samples et stems d'un beatmaker dans un catalogue clair (nom, durée, BPM, tonalité estimée, date, dossier) sans jamais toucher aux fichiers originaux. Produit une page HTML consultable et un fichier tableur (CSV), et peut proposer un plan de rangement validé avant toute action. Use when the user says "range mes sons", "fais l'inventaire de mes prods", "trouve-moi mes prods à 140 BPM", "catalogue de mes loops", "quelles prods j'ai en Do mineur", "j'ai trop de fichiers", or wants to sort, search or tag audio files.
---

# Catalogue de sons

## Règle absolue

**Ne jamais supprimer, renommer, déplacer ou modifier un fichier audio ou un projet
(FL/Ableton/Logic) d'origine.** Le catalogue est créé à côté, dans
`~/Claude/projets/catalogue-sons/`. Tout rangement est proposé sous forme de plan, validé par
lui, et se fait par **copie** (les originaux restent où ils sont).

## 0. Sauvegarde d'abord

Avant la toute première analyse, demande-lui s'il a une sauvegarde de ses prods (disque externe
ou cloud). S'il n'en a pas, propose de la faire en premier (copie vers un disque externe ou un
dossier Google Drive / iCloud), et ne commence qu'après sa réponse.

## 1. Trouver les sons

Demande-lui où sont ses prods (ou cherche dans les dossiers habituels : Musique, Documents,
Desktop, dossiers de FL Studio / Ableton / Logic). Montre-lui ce que tu as trouvé (nombre de
fichiers par dossier) avant d'analyser.

Formats : wav, mp3, aiff, flac, m4a. Ignore les fichiers de moins d'une seconde.

## 2. Analyser

- Durée, date, taille : avec `ffprobe` (paquet `ffmpeg`). Installe-le si absent
  (Mac : `brew install ffmpeg` ; Windows : `winget install ffmpeg`).
- BPM et tonalité : estimation automatique avec un petit script Python (librairie `librosa`,
  installée dans un environnement isolé dans le dossier du projet). Préviens-le que c'est une
  estimation : à vérifier à l'oreille, surtout pour la tonalité.
- Si le nom du fichier contient déjà un BPM ou une tonalité (ex : `dark_140_Cmin.wav`),
  privilégie ce que lui a écrit.
- Gros volume (plus de 300 fichiers) : préviens que ça peut prendre du temps, traite par lots.

## 3. Livrer

- `catalogue.csv` : ouvrable dans Excel / Numbers / Google Sheets.
- `catalogue.html` : une page avec recherche et filtres (BPM, tonalité, dossier) et un lecteur
  pour écouter chaque son directement. Ouvre-la dans son navigateur.
- Résumé en 3 lignes : combien de sons, les plages de BPM les plus fréquentes, les doublons
  probables (même durée et même nom approchant) signalés sans rien supprimer.

## 4. Rechercher

« Trouve-moi mes prods entre 140 et 150 BPM en mineur » : réponds depuis le catalogue,
avec le chemin de chaque fichier. Si le catalogue a plus d'un mois, propose de le rafraîchir.
