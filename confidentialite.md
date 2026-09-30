# Politique de confidentialité de ModelTV

Dernière mise à jour : 30 septembre 2026

ModelTV est un lecteur vidéo pour Android, Android TV et Google TV. Il lit les playlists M3U et les accès Xtream que vous fournissez vous-même. **ModelTV ne fournit aucune chaîne, aucun film ni aucun abonnement.**

Cette politique décrit les données que ModelTV utilise, où elles vont et combien de temps elles sont conservées. Elle s’applique aux versions Google Play et GitHub de l’application.

Responsable : le développeur de ModelTV, joignable à **benjamin.dagbert@gmail.com**.

## 1. Ce qui reste sur votre appareil

- **Vos playlists** : adresses M3U, serveurs Xtream, noms d’utilisateur et mots de passe. Ils sont enregistrés uniquement sur l’appareil et ne sont jamais envoyés au serveur ModelTV. L’application les utilise pour contacter directement votre fournisseur. Pour configurer un téléviseur, un téléphone peut lui transmettre la playlist directement sur votre réseau local, de façon chiffrée, sans passer par le serveur ModelTV.
- Votre bibliothèque, vos profils, favoris, historique, progressions et réglages, tant que vous n’utilisez pas de compte ModelTV.
- Le diagnostic du dernier plantage (Réglages → À propos), qui ne contient ni adresse ni identifiant et n’est envoyé nulle part.

Désinstaller ModelTV efface ces données.

## 2. Ce qui est envoyé, même sans compte

- **Serveur ModelTV** (Google Firebase, région Paris) : au lancement de l’application, un **identifiant pseudonyme de l’appareil** (empreinte calculée à partir de l’identifiant Android, qui ne permet pas de retrouver ce dernier), la version et la variante de l’application. Le serveur conserve la date du premier lancement, la date du dernier contact, la version et la variante. Cela sert à transmettre des informations de service (par exemple une mise à jour nécessaire) et à gérer une éventuelle période d’essai. Cet identifiant n’est enregistré ni avec votre compte ni avec votre adresse e-mail ; il est effacé deux ans après le dernier contact de l’appareil. Pour limiter les abus, le serveur compte les demandes par empreinte de l’adresse IP et par minute ; ces compteurs sont effacés automatiquement sous 48 heures.
- **TMDb** (The Movie Database) : les titres et années des films et séries de votre playlist, pour obtenir affiches, résumés et distributions. TMDb reçoit aussi votre adresse IP, comme tout site consulté. Les informations reçues sont conservées sur l’appareil six mois au plus. Politique de TMDb : https://www.themoviedb.org/privacy-policy
- **IntroDB** : l’identifiant IMDb, la saison et l’épisode d’une série, pour connaître la position de son générique.
- **YouTube** : une bande-annonce s’ouvre dans l’application ou le site YouTube, soumis aux règles de Google.
- **Google Cast** : quand vous diffusez sur un téléviseur, l’adresse de la vidéo est transmise à l’appareil Cast.
- **Votre fournisseur IPTV** reçoit les demandes de lecture et de catalogue, comme avec tout lecteur.

## 3. Avec un compte ModelTV (facultatif)

Le compte sert à synchroniser vos appareils. Il utilise la connexion Google (Firebase Authentication) ou, sur un téléviseur, un QR code approuvé depuis un téléphone déjà connecté.

- **Identité** : adresse e-mail, nom et photo de votre compte Google, et un identifiant de compte technique.
- **Données synchronisées** : profils (nom, couleur, avatar), favoris, historique et progressions de lecture (titres, identifiants TMDb, positions), réglages d’apparence et de lecture, chaînes favorites, catégories personnelles, chaînes récemment regardées, règles de regroupement des chaînes. Les réglages propres à une playlist sont rangés sous une empreinte anonyme de la playlist : **jamais son adresse ni ses identifiants**.
- **Connexion d’un téléviseur** : une session de cinq minutes avec le nom de l’appareil, effacée automatiquement sous 48 heures.
- **Sécurité de la connexion** : Firebase Authentication traite aussi l’adresse IP et le type d’appareil (agent utilisateur) pour prévenir les abus.
- **Trakt** (si vous l’associez) : les jetons d’accès Trakt sont conservés sur le serveur ModelTV, sans être lisibles par l’application, et les titres que vous avez vus avec les profils associés sont envoyés à Trakt. Politique de Trakt : https://trakt.tv/privacy

Ces données sont hébergées par Google Firebase et conservées jusqu’à la suppression du compte.

## Services Google intégrés

ModelTV utilise des bibliothèques de Google qui transmettent à Google des données techniques, selon les [règles de confidentialité de Google](https://policies.google.com/privacy) :

- **Firebase** (compte, synchronisation, serveur ModelTV) : adresse IP et agent utilisateur des requêtes.
- **Google Cast** : journaux d’utilisation anonymes (découverte des appareils, sessions de diffusion, modèle de l’appareil), sans identifiant permettant de remonter à vous.
- **Scanner de QR code** des services Google Play : métriques de performance et d’utilisation du scanner.

## 4. Supprimer votre compte

- Dans l’application : **Réglages → Compte & profils → Supprimer mon compte**. Les profils, favoris, historiques, progressions et réglages synchronisés sont effacés du serveur, les comptes Trakt associés sont déconnectés (jetons révoqués), les connexions de téléviseurs et l’éventuel accès offert à votre adresse sont effacés, puis le compte lui-même est supprimé.
- Sans l’application : suivez https://b-dagbert.github.io/ModelTV-Releases/suppression-compte.html

## 5. Ce que ModelTV ne fait pas

- Aucune publicité. Aucun outil de mesure d’audience ni de suivi publicitaire : seules les données techniques des services Google décrits plus haut leur sont transmises.
- Aucune vente ni location de données.
- Aucun contenu audiovisuel fourni : vous êtes responsable de disposer des droits sur les playlists que vous utilisez.

## 6. Sécurité

Les échanges avec le serveur ModelTV, TMDb, IntroDB et Trakt sont chiffrés (HTTPS). Les échanges avec votre fournisseur utilisent l’adresse que vous avez saisie : **si elle commence par http://, votre nom d’utilisateur, votre mot de passe et les flux vidéo circulent sans chiffrement** et peuvent être lus sur le réseau. Avant d’enregistrer une telle playlist, ModelTV le signale, cherche si le fournisseur répond aussi en https:// et, si c’est le cas, propose cette adresse chiffrée. Les données du compte ne sont accessibles qu’à ce compte.

## 7. Enfants

ModelTV ne s’adresse pas aux enfants de moins de 13 ans et ne collecte pas sciemment leurs données.

## 8. Vos droits

Vous pouvez demander l’accès à vos données, leur rectification, leur suppression, leur portabilité ou vous opposer à leur traitement en écrivant à **benjamin.dagbert@gmail.com**. Vous pouvez aussi saisir la CNIL (www.cnil.fr).

## 9. Modifications

Toute modification de cette politique est publiée à cette adresse avec sa date de mise à jour.

---

## Privacy policy (English summary)

ModelTV is a video player for playlists (M3U, Xtream) supplied by the user; it provides no content. Playlist addresses and credentials stay on the device and are never sent to the ModelTV server. Without an account, the app sends the ModelTV server (Google Firebase, Paris region) a pseudonymous device identifier derived from the Android ID, with the app version, to deliver service notices and manage a possible trial (erased two years after the device's last contact); titles are sent to TMDb for artwork and summaries, and IMDb episode ids to IntroDB. With an optional account (Google sign-in), the Google e-mail, name and photo and the synchronised profiles, favourites, watch history, progress and settings are stored in Firebase until the account is deleted. Linked Trakt accounts receive the watched history. Google libraries (Firebase, Cast, the Play services QR scanner) send Google technical data such as IP address, user agent and anonymous usage logs. No ads, no analytics tools, no sale of data. Traffic with the ModelTV server, TMDb, IntroDB and Trakt is encrypted (HTTPS); if the provider address entered by the user starts with http://, the provider credentials and the video streams travel unencrypted: the app warns before saving such a playlist and offers the https:// address when the provider answers there. Delete the account in the app (Settings → Account & profiles → Delete my account) or through https://b-dagbert.github.io/ModelTV-Releases/suppression-compte.html. Contact: **benjamin.dagbert@gmail.com**.
