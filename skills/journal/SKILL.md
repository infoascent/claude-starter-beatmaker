---
name: journal
description: Tient le journal de travail dans ~/Claude/memoire/journal.md pour ne jamais perdre le fil d'une session à l'autre. Ajoute une entrée datée en haut du fichier (ce qui a été fait, décidé, appris, la suite). Use when the user says "note ça", "garde une trace", "mets ça dans le journal", "on en était où", "qu'est-ce qu'on a fait la dernière fois", "résume la session", or at the end of any session that moved a project forward.
---

# Journal

Fichier : `~/Claude/memoire/journal.md` (le créer avec un titre « # Journal » s'il n'existe pas).

## Écrire une entrée

Ajoute la nouvelle entrée **en haut**, sous le titre, au format :

```
## AAAA-MM-JJ : <sujet en quelques mots>
- Fait : <ce qui a été produit, avec le chemin des fichiers ou l'adresse du site>
- Décidé : <les choix pris, s'il y en a>
- Appris sur moi : <préférence ou info durable, s'il y en a>
- La suite : <la prochaine action concrète>
```

Court : 3 à 6 lignes. Les lignes vides de sens sont omises.
Si une info « Appris sur moi » est durable, propose aussi de l'ajouter à `~/.claude/CLAUDE.md`.

## Relire (« on en était où ? »)

Lis les 3 dernières entrées et réponds en 3 lignes : où on en est, ce qui reste, ce que tu
proposes de faire maintenant.

## Quand l'utiliser sans qu'on te le demande

À la fin d'une session qui a fait avancer quelque chose. Dis-le en une ligne
(« J'ai noté ça dans ton journal. »). Pas pour une simple question.
