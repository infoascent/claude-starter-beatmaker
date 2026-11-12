---
name: apprendre
description: Mini-cours interactif de prise en main de Claude Code pour un débutant total (beatmaker, zéro connaissance en code). 7 leçons de 5 minutes, chacune avec un vrai résultat concret. Reprend automatiquement là où il s'était arrêté grâce à ~/Claude/memoire/progression.md. Use when the user types /apprendre, says "on reprend le cours", "leçon suivante", "apprends-moi Claude Code", "je comprends pas comment ça marche", or asks how Claude Code works in general.
---

# Apprendre Claude Code (cours express)

## Comment donner le cours

1. Lis `~/Claude/memoire/progression.md` pour savoir quelle leçon est la prochaine.
   S'il n'existe pas, crée-le et commence à la leçon 1.
2. Une leçon à la fois. Format de chaque leçon :
   - **L'idée** en 3 à 5 lignes max, avec une image du monde de la musique.
   - **On le fait** : un exercice concret où c'est LUI qui écrit la demande à Claude
     (donne-lui la phrase exemple, il la tape ou la reformule à sa façon). Il apprend en faisant.
   - **À retenir** : une phrase.
3. À la fin de chaque leçon : mets à jour `progression.md` (leçon terminée + date), puis
   demande « on enchaîne sur la suivante ou on s'arrête là ? ».
4. Ton : pote qui s'y connaît, pas prof. Jamais de pavé. S'il pose une question hors sujet,
   réponds-y, c'est bon signe.
5. S'il a fini les 7 leçons : félicite-le en une ligne, et propose 3 projets tirés de son profil
   (section « Qui je suis » de son CLAUDE.md), en commençant par ce qui lui fait gagner du temps.

---

## Leçon 1 : Claude Code, c'est quoi la différence avec le chat ?

**L'idée.** Le Claude « normal » te répond. Claude Code **agit sur ton ordi** : il crée des
dossiers, écrit des fichiers, installe des outils, ouvre ton navigateur, range tes sons. C'est la
différence entre un pote qui t'explique comment mixer et un ingé son assis à ta place.
Tout ce qu'il fait se passe dans le dossier que tu lui as ouvert (`Claude`), et partout où tu
l'autorises.

**On le fait.** Demande-lui : « Crée un dossier test dans mes projets, avec dedans un fichier
qui liste 5 idées de noms pour ma prochaine tape. » Puis : « Ouvre-moi ce dossier. »
(Ouvre-le réellement dans le Finder ou l'Explorateur pour qu'il voie que c'est vrai.)

**À retenir.** Tu décris le résultat que tu veux, Claude fait le travail sur ta machine.

## Leçon 2 : la mémoire (pourquoi il te connaît déjà)

**L'idée.** Chaque nouvelle conversation, Claude repart de zéro, comme une session studio où
l'ingé a tout oublié. Sauf ce qui est **écrit dans des fichiers**. Ton fichier `CLAUDE.md`
(ton « cerveau ») est relu à chaque fois : ton style, tes objectifs, tes règles. Et ton
`journal.md` garde la trace de ce qu'on a fait.
Règle d'or : un truc important qui n'est pas écrit dans un fichier sera oublié.

**On le fait.** Montre-lui son CLAUDE.md (ouvre-le). Puis fais-lui dire :
« Ajoute à ma mémoire que [une vraie préférence à lui, ex : je bosse surtout la nuit / je veux
toujours des réponses courtes]. » Vérifie avec lui que c'est bien écrit dedans.

**À retenir.** « Ajoute à ma mémoire que... » : c'est comme ça que Claude devient ton Claude.

## Leçon 3 : les skills (tes presets)

**L'idée.** Un skill, c'est un preset : une recette écrite une fois, que Claude recharge quand il
faut. Tu en as 6 installés (montre la liste avec une ligne chacun). Tu peux les lancer en tapant
`/` ou juste en demandant normalement. Et surtout : **tu peux en créer** pour n'importe quelle
tâche que tu refais souvent. Pas besoin de code, Claude l'écrit.

**On le fait.** Demande-lui une tâche qu'il refait souvent (ex : préparer l'envoi d'un pack de
prods, écrire sa bio pour une plateforme, nommer ses fichiers). Puis fais-lui dire :
« Crée-moi un skill qui fait ça à chaque fois que je te le demande. »
Crée le skill dans `~/.claude/skills/<nom>/SKILL.md`, puis teste-le avec lui.

**À retenir.** Tu fais un truc 3 fois ? Transforme-le en skill.

## Leçon 4 : ton premier site (le moment wow)

**L'idée.** Claude sait créer un site complet en quelques minutes. Pas un template moche :
un vrai site, à ton image. On le crée sur ton ordi d'abord, on le met en ligne en leçon 7.

**On le fait.** Lance le skill `site-web` : un site vitrine de beatmaker (nom, bio, style,
lecteur avec 3 prods, contact). Pose-lui 3 questions max (nom affiché, ambiance visuelle,
couleurs), construis, ouvre-le dans son navigateur. Puis fais-lui demander une modif à voix
haute, du genre « mets le fond plus sombre et la typo plus agressive », pour qu'il voie qu'on
itère en parlant.

**À retenir.** Tu décris, tu regardes, tu corriges en parlant. Comme une session de mix.

## Leçon 5 : bien parler à Claude (les 5 réflexes)

**L'idée.** La qualité du résultat dépend de la demande. Les 5 réflexes :
1. **Le résultat, pas la méthode** : « je veux un site où un artiste peut écouter et me
   contacter » plutôt que « fais du HTML ».
2. **Le contexte** : pour qui, pourquoi, avec quels exemples (« dans le style de tel site »).
3. **Un sujet = une conversation.** Nouveau sujet : nouvelle conversation. Sinon il se mélange.
4. **Gros chantier : demande d'abord le plan.** « Propose-moi un plan avant de faire. »
5. **Il se trompe ? Dis-le simplement.** « Non, c'est pas ça, je voulais X. » Il corrige.
Bonus : tu peux lui envoyer des captures d'écran et des fichiers, il les comprend.

**On le fait.** Prends une demande floue qu'il pourrait faire (ex : « fais-moi un post Insta »),
et réécris-la avec lui en appliquant les réflexes. Exécute la bonne version.

**À retenir.** Plus tu donnes de contexte, moins tu corriges.

## Leçon 6 : connecteurs, MCP, API (brancher Claude à tes outils)

**L'idée.** Par défaut, Claude voit ton ordi et internet. Pour qu'il agisse dans tes outils
(Gmail, Google Drive, Notion, Instagram...), il faut le **brancher**. Trois mots, une seule idée :
- **API** : la prise électrique d'un service. Chaque service a la sienne.
- **Clé API** : le code d'accès à cette prise. Ça se garde comme un mot de passe
  (dans `~/Claude/memoire/secrets.env`, jamais dans le chat).
- **MCP / connecteur** : la multiprise toute prête qui branche Claude à un service sans qu'il
  doive tout recâbler. Les plus simples s'ajoutent en 2 clics dans les réglages de l'app Claude
  (Paramètres > Connecteurs).
Pas besoin d'en installer maintenant : tu le feras le jour où un projet le demande, et Claude
s'en occupe. La liste des plus utiles pour toi est dans `~/Claude/memoire/guide.md`
(résume-la-lui en 4 lignes).

**On le fait.** Demande-lui quel outil il utilise le plus (Gmail, Drive, Notion, Insta...).
S'il a un connecteur officiel dans l'app, guide-le pour l'activer dans les réglages, puis fais
un test simple (ex : « cherche dans mes mails le dernier échange avec tel artiste »).
S'il n'en veut pas : passe, aucun souci.

**À retenir.** Un outil que Claude ne voit pas, ça se branche. Et une clé API ne se colle jamais
dans le chat.

## Leçon 7 : mettre en ligne (GitHub et Vercel en 5 minutes)

**L'idée.** Pour que ton site soit visible par tout le monde, il faut le mettre sur internet.
- **GitHub** : un coffre-fort en ligne pour tes projets, avec l'historique de chaque version
  (comme garder toutes les versions d'une prod). Gratuit.
- **Vercel** : l'hébergeur qui transforme ce coffre en vrai site avec une adresse. Gratuit aussi.
Claude fait tout. Lui crée juste les comptes (c'est lui qui doit cliquer et valider les mails).

**On le fait.** Avec le skill `site-web`, étape « mise en ligne » : installe ce qui manque,
fais-lui créer son compte GitHub puis Vercel (connexion avec GitHub), publie, et donne-lui
l'adresse du site. Fais-lui l'ouvrir sur son téléphone.

**À retenir.** Ton site est en ligne, et chaque modif que tu demandes à Claude peut être
republiée en une phrase : « mets à jour le site ».
