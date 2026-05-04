# 🎬 Analyseur de Vidéos Bilibili

> Un outil léger, rapide et polyvalent pour extraire du contenu vidéo de Bilibili (Version éducative et de recherche)

[🌐 Démo en ligne](https://twittervideodownloaderx.com/bilibili_downloader_fr) • [📝 Guide d'utilisation](#-guide-dutilisation) • [❓ Questions fréquentes](#-questions-fréquentes)

---

## 📋 Présentation du projet

Ce projet est un outil d'analyse vidéo basé sur le web, conçu pour extraire en toute sécurité les métadonnées des ressources multimédias à partir de vidéos publiques sur la plateforme Bilibili (哔哩哔哩), tout en proposant des options de conversion de format et d'enregistrement local. Aucune installation de logiciel client ni création de compte requise : utilisez-le directement depuis votre navigateur.

> ⚠️ **Avertissement important** : Cet outil est destiné exclusivement à un usage personnel d'apprentissage, de recherche technique et dans le cadre d'une utilisation raisonnable. Veuillez respecter les [Directives de la Communauté Bilibili](https://www.bilibili.com/blackboard/protocol.html), la 《Loi sur le droit d'auteur de la République populaire de Chine》ainsi que les autres réglementations applicables. Respectez le travail des créateurs ; n'utilisez pas le contenu téléchargé à des fins commerciales ou pour porter atteinte aux droits d'autrui.

---

## ✨ Fonctionnalités principales

- 🔗 **Analyse de liens** : Compatible avec les URLs standards de vidéos/animés Bilibili ; détection automatique des épisodes et des options de résolution disponibles
- 📥 **Export multi-formats** :
  - Flux vidéo original (prend en charge les résolutions publiques comme 1080P/720P, etc.)
  - Extraction audio → Format MP3 (pratique pour écouter des cours/musique hors ligne)
  - Extrait vidéo → Conversion en GIF animé (idéal pour créer des mèmes/démonstrations éducatives)
- 🌍 **Interface multilingue** : Prise en charge du français, anglais, chinois, japonais, coréen et plus encore
- 📱 **Compatibilité multiplateforme** : Fonctionne parfaitement sur Chrome / Firefox / Safari / Edge ; expérience optimisée pour les appareils mobiles et tablettes
- 🔒 **Respect de la vie privée** : Aucune connexion à un compte Bilibili requise, aucune collecte de données personnelles ; processus d'analyse entièrement anonyme
- ⚡ **Traitement rapide** : L'analyse se termine en moyenne en 5 à 10 secondes ; prise en charge des requêtes simultanées et du traitement par lots

---

## 🚀 Démarrage rapide

### Utilisation en ligne (recommandée)
1. Accédez à [https://twittervideodownloaderx.com/bilibili_downloader_fr](https://twittervideodownloaderx.com/bilibili_downloader_fr)
2. Copiez le lien de la vidéo cible (exemple : `https://www.bilibili.com/video/BV1xx411c7mD`)
3. Collez le lien dans le champ de saisie → Cliquez sur le bouton 「Analyser」
4. Sélectionnez la résolution et le format souhaités → Enregistrez le fichier selon les instructions du navigateur

### Déploiement local (pour développeurs)
```bash
# Cloner le dépôt
git clone https://github.com/your-repo/bili-video-parser.git

# Installer les dépendances
cd bili-video-parser && npm install

# Configurer les variables d'environnement (optionnel)
cp .env.example .env

# Démarrer le serveur de développement
npm run dev
```

> 💡 Note : Ce projet utilise une architecture basée sur Node.js + Express. Consultez la documentation détaillée de déploiement dans `/docs/DEPLOY.md`

---

## 🛠 Stack technique

| Module | Technologies utilisées |
|--------|------------------------|
| Frontend | Vue 3 + TypeScript + Vite |
| Backend | Node.js + Express + Axios |
| Traitement vidéo | ffmpeg.wasm (conversion légère côté client) |
| Proxy de relais | Cloudflare Workers / Middleware personnalisé |
| Internationalisation | vue-i18n + Packs de langues JSON |

---

## 📚 Guide d'utilisation

### Flux d'opération de base
```
1. Obtenir le lien de la vidéo
   └─ Ouvrez la vidéo cible sur Bilibili → Copiez l'URL depuis la barre d'adresse du navigateur

2. Envoyer la demande d'analyse
   └─ Collez le lien dans le champ de saisie de l'outil → Cliquez sur 「Démarrer l'analyse」

3. Sélectionner la configuration de sortie
   ├─ 🎬 Télécharger la vidéo : Choisir la résolution (360P/720P/1080P, etc. - options publiques uniquement)
   ├─ 🎵 Extraire l'audio : Générer un fichier MP3 (idéal pour écouter des cours/musique hors ligne)
   └─ 🎞 Générer un GIF : Créer une animation à partir d'une plage de temps spécifiée (recommandé : ≤15 secondes)

4. Enregistrer le fichier
   └─ La ressource s'ouvrira dans un nouvel onglet → Clic droit/menu → 「Enregistrer sous」
```

### Conseils pour l'utilisation sur mobile
- iOS Safari : Bouton Partager → 「Enregistrer dans Fichiers」
- Android Chrome : Appui long sur l'aperçu de la vidéo → 「Télécharger la vidéo」
- Si la vidéo se lance automatiquement : Cliquez sur `⋮` en haut à droite du lecteur → Sélectionnez 「Télécharger」

---

## ❓ Questions fréquentes

**Q : Où sont enregistrés les fichiers téléchargés ?**  
R : Les fichiers sont enregistrés dans le dossier de téléchargement configuré dans votre navigateur. Vous pouvez vérifier ou modifier ce chemin dans les paramètres du navigateur.

**Q : Puis-je analyser du contenu réservé aux membres ou nécessitant une connexion ?**  
R : Non. Cet outil ne fonctionne qu'avec des vidéos configurées comme publiques et respecte les paramètres d'accès du contenu d'origine.

**Q : La qualité image/audio est-elle réduite après conversion ?**  
R : Les téléchargements vidéo conservent le débit binaire d'origine de la résolution sélectionnée. Le format MP3 utilise un encodage standard à 128 kbps. Le format GIF optimise le taux d'images en fonction de la durée pour équilibrer taille du fichier et fluidité.

**Q : L'historique de téléchargement ou le cache sont-ils stockés ?**  
R : Non. Toutes les ressources sont transmises directement à l'appareil de l'utilisateur via un proxy temporaire ; le serveur ne conserve aucune requête ni fichier multimédia.

**Q : Que faire si l'analyse échoue ?**  
R : Veuillez vérifier : ① Que le lien pointe vers une vidéo publique valide ② Que votre connexion internet soit stable ③ Essayez avec un autre navigateur. Si le problème persiste, n'hésitez pas à le signaler via un Issue.

---

## ⚖️ Conformité réglementaire et Clause de non-responsabilité

- Cet outil **ne contourne ni ne viole aucune mesure de protection technique** de la plateforme ; il se contente d'obtenir des métadonnées via des interfaces publiques
- L'utilisateur est responsable de vérifier que son usage est conforme à la législation locale et aux conditions d'utilisation de la plateforme
- Cas d'usage recommandés : Archivage personnel pour l'apprentissage, démonstrations éducatives, matériel de référence pour la création de contenu... toujours dans le cadre de l'usage loyal (Fair Use)
- Si vous identifiez un contenu susceptible de porter atteinte à des droits, veuillez contacter le canal officiel via le [formulaire de signalement de droits d'auteur de Bilibili](https://www.bilibili.com/blackboard/help.html#copyright)

---

## 🤝 Guide de contribution

Nous accueillons avec plaisir vos Pull Requests et signalements d'Issues ! Avant de contribuer, veuillez consulter :
- [Standards de code](/CONTRIBUTING.md)
- [Guide de traduction multilingue](/locales/README.md)
- [Exigences de sécurité et de conformité](/SECURITY.md)

---

## 📄 Licence

Ce projet est publié sous la [Licence MIT](/LICENSE). Il peut être utilisé gratuitement à des fins éducatives et de recherche. Pour un usage commercial, veuillez vérifier attentivement le respect des réglementations légales applicables.

---

> 🌟 Si cet outil vous a été utile, n'hésitez pas à ✨lui attribuer une Étoile (Star) ! Votre soutien est la plus grande motivation pour que nous continuions à maintenir et améliorer ce projet~

*Dernière mise à jour : Mai 2026 | Version : v1.0.0*