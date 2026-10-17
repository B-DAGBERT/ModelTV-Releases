# Politique de confidentialité de ModelTV

Dernière mise à jour : 17 octobre 2026

ModelTV est un lecteur vidéo pour Android, Android TV, Google TV, Fire TV, iPhone, iPad et Apple TV. Il lit les playlists M3U et les accès Xtream que vous fournissez vous-même. **ModelTV ne fournit aucune chaîne, aucun film ni aucun abonnement.**

Cette politique décrit les données que ModelTV utilise, où elles vont et combien de temps elles sont conservées. Elle s’applique à toutes les versions de l’application : Google Play, GitHub et App Store (TestFlight compris).

Responsable : le développeur de ModelTV, joignable à **contact@modeltv.app**.

## 1. Ce qui reste sur votre appareil

- **Vos playlists** : adresses M3U, serveurs Xtream, noms d’utilisateur et mots de passe. Sans compte ModelTV, elles restent uniquement sur l’appareil ; avec un compte, elles sont aussi gardées dans votre compte, chiffrées de bout en bout (voir la partie 3). L’application les utilise pour contacter directement votre fournisseur. Pour les transmettre à un autre de vos appareils, « Ajouter un appareil » les chiffre sur votre appareil pour le seul appareil qui les reçoit : le serveur ModelTV ne fait que relayer un paquet illisible (voir la partie 2).
- Votre bibliothèque, vos profils, favoris, historique, progressions et réglages, tant que vous n’utilisez pas de compte ModelTV.
- Sur Android, le diagnostic du dernier plantage (Réglages → À propos), qui ne contient ni adresse ni identifiant et n’est envoyé nulle part.

Désinstaller ModelTV efface ces données.

## 2. Ce qui est envoyé, même sans compte

- **Serveur ModelTV** (Google Firebase, région Paris) : au lancement de l’application (et, sur iPhone, iPad et Apple TV, au retour dans l’application, au plus toutes les trois heures), un **identifiant pseudonyme de l’appareil** (empreinte calculée à partir de l’identifiant Android ou, sur les appareils Apple, d’un identifiant aléatoire gardé dans le trousseau de l’appareil, qui ne permet pas de retrouver ce dernier), la version et la variante de l’application. Le serveur conserve la date du premier lancement, la date du dernier contact, la version et la variante. Cela sert à transmettre des informations de service (par exemple une mise à jour nécessaire) et, sur Android, à gérer une éventuelle période d’essai. Cet identifiant n’est enregistré ni avec votre compte ni avec votre adresse e-mail ; il est effacé deux ans après le dernier contact de l’appareil. Pour limiter les abus, le serveur compte les demandes par empreinte de l’adresse IP, par minute ou par heure ; ces compteurs sont effacés automatiquement sous 48 heures.
- **Ajout d’un appareil** (avec ou sans compte) : quand vous transmettez des playlists ou votre compte d’un appareil à un autre, le serveur ModelTV ouvre une session de cinq minutes (dix une fois l’autre appareil arrivé) avec le nom, le type et la plateforme de chaque appareil, la version de l’application, leurs clés publiques, un code court et le paquet chiffré pour l’appareil qui le reçoit, illisible pour ModelTV. Le paquet est effacé dès sa réception, sinon la session l’est automatiquement sous 72 heures.
- **TMDb** (The Movie Database) : les titres et années des films et séries de votre playlist, pour obtenir affiches, résumés et distributions. TMDb reçoit aussi votre adresse IP, comme tout site consulté. Les informations reçues sont conservées sur l’appareil six mois au plus. Politique de TMDb : https://www.themoviedb.org/privacy-policy
- **IntroDB** : l’identifiant IMDb, la saison et l’épisode d’une série, pour connaître la position de son générique.
- **YouTube** : une bande-annonce s’ouvre dans l’application ou le site YouTube, soumis aux règles de Google.
- **Google Cast** (Android) et **AirPlay** (iPhone, iPad) : quand vous diffusez sur un téléviseur, l’adresse de la vidéo est transmise à l’appareil qui la lit.
- **Recherche vocale sur iPhone et iPad** : votre voix est traitée par la reconnaissance vocale d’Apple, sur l’appareil quand il le permet, sinon par les serveurs d’Apple, selon les règles d’Apple.
- **Votre fournisseur IPTV** reçoit les demandes de lecture et de catalogue, comme avec tout lecteur.

## 3. Avec un compte ModelTV (facultatif)

Le compte sert à synchroniser vos appareils. Il utilise la connexion Google ou Apple (Firebase Authentication) ou, sur un appareil qui ne se connecte pas lui-même (un téléviseur), « Ajouter un appareil » depuis un appareil déjà connecté.

- **Identité** : adresse e-mail, nom et photo de votre compte Google, ou adresse e-mail (éventuellement l’adresse relais d’Apple qui masque la vôtre) et nom de votre identifiant Apple, et un identifiant de compte technique.
- **Playlists (chiffrées de bout en bout)** : adresses, serveurs, noms d’utilisateur et mots de passe sont chiffrés sur vos appareils avec une clé propre à votre compte, que seuls vos appareils détiennent. Le serveur ModelTV ne garde que des paquets illisibles, avec leur date de modification et un marqueur de suppression ; ni ModelTV ni Google ne peuvent les lire. Si vous perdez tous vos appareils, ces playlists ne peuvent pas être récupérées : il faut les saisir à nouveau.
- **Clé du compte** : créée sur un de vos appareils, transmise à vos autres appareils uniquement chiffrée pour chacun d’eux (à l’ajout d’un appareil, ou quand un appareil déjà connecté l’autorise).
- **Vos appareils** : pour chaque appareil connecté, un identifiant aléatoire, son nom (modifiable), son type et sa plateforme, la version de l’application, la date d’ajout, la date de dernière activité (mise à jour environ une fois par jour), une clé publique et l’état de son accès aux playlists. Cela sert à « Mes appareils » et à la déconnexion à distance.
- **Déconnexion à distance** : l’appareil déconnecté efface, à sa prochaine connexion à Internet, la clé du compte et les playlists synchronisées ; un appareil resté hors ligne garde ce qu’il avait jusque-là.
- **Données synchronisées** : profils (nom, couleur, avatar), favoris, historique et progressions de lecture (titres, identifiants TMDb, positions), réglages d’apparence et de lecture, affichage des catégories du fournisseur, chaînes favorites, catégories personnelles, chaînes récemment regardées, règles de regroupement des chaînes. Les règles de regroupement d’une playlist sont rangées sous l’identifiant aléatoire de cette playlist : **jamais son adresse ni ses identifiants** (les playlists elles-mêmes sont chiffrées, voir ci-dessus).
- **Ajout d’un appareil avec le compte** : en plus de la session décrite dans la partie 2, l’identifiant du compte, pour connecter l’appareil qui reçoit.
- **Sécurité de la connexion** : Firebase Authentication traite aussi l’adresse IP et le type d’appareil (agent utilisateur) pour prévenir les abus.
- **Trakt** (si vous l’associez) : les jetons d’accès Trakt sont conservés sur le serveur ModelTV, sans être lisibles par l’application, et les titres que vous avez vus avec les profils associés sont envoyés à Trakt. Politique de Trakt : https://trakt.tv/privacy

Ces données sont hébergées par Google Firebase et conservées jusqu’à la suppression du compte.

### Services Google intégrés

ModelTV utilise des services de Google qui reçoivent des données techniques, selon les [règles de confidentialité de Google](https://policies.google.com/privacy) :

- **Firebase** (compte, synchronisation, serveur ModelTV, relais de l’ajout d’un appareil ; toutes les versions) : adresse IP et agent utilisateur des requêtes. Firebase héberge aussi les paquets chiffrés des playlists et la liste des appareils du compte (voir la partie 3).
- **Google Cast** (Android) : journaux d’utilisation anonymes (découverte des appareils, sessions de diffusion, modèle de l’appareil), sans identifiant permettant de remonter à vous.
- **Scanner de QR code** des services Google Play (Android) : métriques de performance et d’utilisation du scanner.

Les applications iPhone, iPad et Apple TV n’intègrent aucune bibliothèque de Google : elles appellent directement les services web de Firebase, et l’iPhone lit les QR codes avec son appareil photo, sans service tiers.

## 4. Supprimer votre compte

- Dans l’application : **Réglages → Compte et appareils → Supprimer mon compte**. Les profils, favoris, historiques, progressions et réglages synchronisés, les playlists chiffrées, la clé du compte chiffrée pour chaque appareil, la liste des appareils et les demandes et autorisations d’accès sont effacés du serveur, les comptes Trakt associés sont déconnectés (jetons révoqués), les sessions d’ajout d’appareil et l’éventuel accès offert à votre adresse sont effacés, puis le compte lui-même est supprimé. Les playlists restent sur l’appareil où vous supprimez le compte, comme playlists de l’appareil seul ; les autres appareils connectés au compte sont déconnectés et peuvent effacer les playlists synchronisées, comme lors d’une déconnexion à distance. Sur iPhone et iPad, pour un compte lié à Apple, une confirmation Apple est demandée et ModelTV renonce aussi à son accès à votre identifiant Apple.
- Sans l’application : suivez https://b-dagbert.github.io/ModelTV-Releases/suppression-compte.html

## 5. Ce que ModelTV ne fait pas

- Aucune publicité. Aucun outil de mesure d’audience ni de suivi publicitaire : seules les données techniques des services Google décrits plus haut leur sont transmises.
- Aucune vente ni location de données.
- Aucun contenu audiovisuel fourni : vous êtes responsable de disposer des droits sur les playlists que vous utilisez.

## 6. Sécurité

Les échanges avec le serveur ModelTV, TMDb, IntroDB et Trakt sont chiffrés (HTTPS). Les playlists synchronisées ou transmises à un autre appareil sont en plus chiffrées de bout en bout avec des algorithmes standard (AES-256-GCM, courbe P-256) ; la clé du compte n’est conservée que sur vos appareils, protégée par leur stockage sécurisé (Android Keystore, trousseau Apple). Les échanges avec votre fournisseur utilisent l’adresse que vous avez saisie : **si elle commence par http://, votre nom d’utilisateur, votre mot de passe et les flux vidéo circulent sans chiffrement** et peuvent être lus sur le réseau. Avant d’enregistrer une telle playlist ou de l’envoyer à un autre appareil, ModelTV le signale, cherche si le fournisseur répond aussi en https:// et, si c’est le cas, propose cette adresse chiffrée. Les données du compte ne sont accessibles qu’à ce compte.

## 7. Enfants

ModelTV ne s’adresse pas aux enfants de moins de 13 ans et ne collecte pas sciemment leurs données.

## 8. Vos droits

Vous pouvez demander l’accès à vos données, leur rectification, leur suppression, leur portabilité ou vous opposer à leur traitement en écrivant à **contact@modeltv.app**. Vous pouvez aussi saisir la CNIL (www.cnil.fr).

## 9. Modifications

Toute modification de cette politique est publiée à cette adresse avec sa date de mise à jour.

---

## Privacy policy (English summary)

ModelTV is a video player for Android, Android TV, Google TV, Fire TV, iPhone, iPad and Apple TV, for playlists (M3U, Xtream) supplied by the user; it provides no content. Without an account, playlists stay on the device. With an account, they are stored end-to-end encrypted: only your devices hold the key; the ModelTV server cannot read them. Adding a device relays an encrypted package for that device only, deleted at reception (otherwise automatically within 72 hours). The account keeps a list of your devices (random identifier, name, type, app version, last activity) for remote disconnection. Every app sends the ModelTV server (Google Firebase, Paris region) a pseudonymous device identifier (derived from the Android ID, or on Apple devices from a random identifier kept in the keychain), with the app version, to deliver service notices such as a required update and, on Android, manage a possible trial (erased two years after the device's last contact); titles are sent to TMDb for artwork and summaries, and IMDb episode ids to IntroDB; on iPhone and iPad, voice search uses Apple's speech recognition (on the device when possible). The video address is passed to the Cast or AirPlay device you choose. With an optional account (Google or Apple sign-in), the Google e-mail, name and photo, or the Apple ID e-mail (possibly Apple's private relay address) and name, the synchronised profiles, favourites, watch history, progress and settings, the encrypted playlists and the device list are stored in Firebase until the account is deleted. Linked Trakt accounts receive the watched history. Google services (Firebase in every version; Cast and the Play services QR scanner on Android only) send Google technical data such as IP address, user agent and anonymous usage logs. No ads, no analytics tools, no sale of data. Traffic with the ModelTV server, TMDb, IntroDB and Trakt is encrypted (HTTPS), and synced or transferred playlists are also end-to-end encrypted (AES-256-GCM, P-256); if the provider address entered by the user starts with http://, the provider credentials and the video streams travel unencrypted: the app warns before saving or sending such a playlist and offers the https:// address when the provider answers there. Delete the account in the app (Settings → Account and devices → Delete my account; on iPhone and iPad, an account linked to Apple also revokes ModelTV's access to the Apple ID) or through https://b-dagbert.github.io/ModelTV-Releases/suppression-compte.html. Contact: **contact@modeltv.app**.
