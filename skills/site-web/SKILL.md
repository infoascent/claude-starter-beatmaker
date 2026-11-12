---
name: site-web
description: Crée un site web de beatmaker / artiste (vitrine, portfolio, lecteur de prods, page de contact, page de vente de beats ou de drumkits) pour un utilisateur qui ne connaît rien au code, l'ouvre en local, puis le met en ligne gratuitement (GitHub + Vercel) et le met à jour sur demande. Use when the user says "fais-moi un site", "crée mon site", "une page pour mes prods", "un portfolio", "mets mon site en ligne", "mets à jour le site", "landing page pour mon drumkit", or wants any web page.
---

# Site web

L'utilisateur ne code pas : il décrit, regarde, corrige en parlant. Tu fais tout le reste.

## 1. Cadrer (3 questions max)

Avant de construire, demande seulement ce qui manque (regarde d'abord son CLAUDE.md) :
- Le but du site : se présenter aux artistes, vendre des prods ou un drumkit, un lien en bio ?
- Le nom affiché et l'ambiance visuelle (2 ou 3 mots : sombre, minimal, street, luxe...).
  S'il a un site qu'il aime, demande le lien et inspire-toi de l'ambiance, sans copier.
- Ce qu'il a déjà : logo, photos, liens (Insta, YouTube, BeatStars, Spotify), prods à mettre.

## 2. Construire

- Dossier : `~/Claude/projets/<nom-du-site>/`.
- Par défaut, un site **statique simple** (HTML + CSS + un peu de JS, sans framework) : rapide,
  gratuit à héberger, rien à installer. Ne passe à un framework que si le besoin l'exige.
- Contenu type d'un site de beatmaker : héro avec nom et accroche, bio courte, lecteur audio
  (fichiers MP3 copiés dans le dossier du site, jamais déplacés depuis leur emplacement
  d'origine, ou embed YouTube/SoundCloud/BeatStars), artistes avec qui il a bossé, liens
  réseaux, contact (lien mailto ou Instagram, pas de formulaire qui nécessite un serveur).
- Soigne le design : typographie forte, vrai parti pris visuel, responsive mobile
  (la plupart des visiteurs viennent d'Instagram sur téléphone). Pas de template générique.
- Textes : écris-les toi-même à partir de son profil, dans son ton. Ne jamais inventer de
  collaboration, de chiffre ou de placement qu'il n'a pas cité.
- Ouvre le site dans son navigateur à la fin, et demande ce qu'il veut changer.

## 3. Mettre en ligne (quand il le demande, ou en leçon 7)

Si l'installation des outils coince (vieux PC, mot de passe oublié, erreur), plan B sans rien
installer : https://app.netlify.com/drop, il glisse le dossier du site dans la page, et c'est en
ligne (compte gratuit pour garder le site). Le plan A ci-dessous reste meilleur pour les mises à
jour en une phrase.


1. Vérifie ce qui est installé (`git`, `gh`, `node`/`npx`). Installe ce qui manque toi-même
   (sur Mac, Homebrew si besoin ; sur Windows, winget). Les installations peuvent demander son
   mot de passe d'ordi : préviens-le en une ligne.
2. **GitHub** : s'il n'a pas de compte, envoie-le sur https://github.com/signup (il doit le
   créer lui-même). Puis connecte `gh` (`gh auth login --web` : il valide dans le navigateur).
   Crée un dépôt pour le site et pousse le code.
3. **Vercel** : envoie-le sur https://vercel.com/signup, « Continue with GitHub » (offre
   gratuite Hobby, **jamais** d'offre payante sans son accord). Puis publie le site
   (import du dépôt GitHub, ou `npx vercel --prod` après `npx vercel login`).
4. Donne-lui l'adresse finale, et dis-lui de l'ouvrir sur son téléphone.
5. Note l'adresse du site et du dépôt dans son journal.

Nom de domaine perso (ex : sonblaze.com) : c'est payant (~10 à 15 € par an). Ne l'achète jamais
toi-même ; explique, et guide-le seulement s'il le veut.

## 4. Mettre à jour

« Mets à jour le site » : fais la modif, montre-la en local, puis pousse sur GitHub
(Vercel republie tout seul) et confirme quand c'est en ligne.
