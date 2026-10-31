# Checklist des tests

**Date** : 31 octobre 2026. **Version testée** : contenu du dossier `eportfolio-github` livré avec ce fichier.
**Résultat de la dernière exécution complète** : **679 contrôles réussis sur 679**.

## Méthode
- Le dossier a été servi par un petit serveur local qui **imite GitHub Pages** : site placé dans un sous-dossier (`/eportfolio/`, comme `https://UTILISATEUR.github.io/eportfolio/`), noms de fichiers sensibles à la casse, et page `404.html` renvoyée pour les adresses inconnues.
- Les tests sont automatisés avec **Playwright**, qui pilote un vrai navigateur et simule la souris, le clavier et le toucher (y compris le pincement à deux doigts). Chaque format a été testé **en français puis en anglais**.
- Les contrôles d’accessibilité sont des **scripts maison** exécutés dans la page (contraste, titres, `alt`, intitulés, focus, tailles). L’outil de référence *axe-core* et le validateur du W3C n’ont pas pu être installés : l’environnement de travail n’a pas accès aux registres de paquets.

## Navigateurs testés
| Navigateur | Testé | Remarque |
|---|---|---|
| Chromium 153.0.8010.12 (moteur de Chrome, Edge, Opera, Samsung Internet) | Oui | Mode sans interface, avec émulation des appareils tactiles |
| Safari (iPhone, iPad, Mac) | **Non** | Moteur WebKit indisponible dans l’environnement. Le code a été adapté aux règles connues de Safari iOS (éléments touchables = vrais boutons, vidéo H.264 avec `playsinline`) et un contrôle vérifie ce point. **À vérifier sur un vrai iPhone après publication.** |
| Firefox | **Non** | Moteur indisponible dans l’environnement. **À vérifier après publication.** |

## Matrice : formats × contrôles
Légende : ✅ FR+EN = réussi en français et en anglais ; — = sans objet pour ce format (par exemple le pincement sur ordinateur, ou la taille des cibles tactiles sans écran tactile).

| Contrôle | PC 1920×1080 | PC 1366×768 | Tab. 1024×768 pays. | Tab. 768×1024 port. | Tél. 390×844 port. | Tél. 844×390 pays. | Tél. 360×800 port. | Tél. 800×360 pays. |
|---|---|---|---|---|---|---|---|---|
| Pas de défilement horizontal | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN |
| Langue du document | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN |
| Ancres du menu valides | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN |
| Clic menu → section Mobilités visible | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN |
| Images affichées chargées | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN |
| Toutes les images des galeries existent (casse exacte) | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN |
| Vidéo elevator speech chargée | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN |
| Galerie : miniature → grande photo | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN |
| Visionneuse ouverte sur la bonne photo | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN |
| Visionneuse : focus sur « Fermer » | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN |
| Visionneuse : suivante | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN |
| Visionneuse : image dans l’écran | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN |
| Visionneuse : fermeture | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN |
| Carte : un point par pays | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN |
| Carte : infobulle (texte, dans la carte) | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN |
| Carte : clic → zoom + panneau | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN |
| Panneau sous la carte (≤860 px) / à côté (>860 px) | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN |
| Italie : Rome et Sicile séparées au zoom | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN |
| Italie : Colisée + Cinecittà en galerie, texte U-571 | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN |
| Sri Lanka : phrase plantations de thé / Lipton | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN |
| Tanzanie : galerie de 6 photos | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN |
| Aucune photo en double dans une galerie ni entre voyages | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN |
| Activités : carrousel surf + agrandissement | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN |
| Activités : photos judo et football, illustrations tennis et boxe | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN |
| CV : onglet anglais | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN |
| Téléchargements CV FR, CV EN, TIPE (fichier PDF reçu) | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN |
| Rôles modèles : « Voir sur la carte » | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN |
| Liens mail, LinkedIn, TIPE, « Voir mon CV » | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN |
| Clavier : 1er Tab = lien d’évitement visible | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN |
| Clavier : lien d’évitement → contenu principal | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN |
| Clavier : focus visible sur les éléments parcourus | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN |
| Contraste AA | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN |
| Hiérarchie des titres sans saut | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN |
| Attribut alt sur toutes les images | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN |
| Boutons et liens avec intitulé accessible | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN |
| Aucun élément ne dépasse de l’écran | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN |
| Aucune image déformée | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN |
| Texte ≥ 12 px | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN |
| Aucune erreur JavaScript / console | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN |
| Aucune ressource introuvable (404) | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN |
| Traduction anglaise (Welcome, rôles modèles, panneau) | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ |
| Carte : pincement à deux doigts | — | — | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN |
| Cibles tactiles ≥ 24 px (hors liens dans le texte) | — | — | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN | ✅ FR+EN |

### Chargements directs (serveur imitant GitHub Pages)
| Adresse | Résultat |
|---|---|
| Chargement direct / | ✅ (code 200) |
| Chargement direct /index.html | ✅ (code 200) |
| Chargement direct /css/style.css | ✅ (code 200) |
| Chargement direct /js/main.js | ✅ (code 200) |
| Chargement direct /404.html | ✅ (code 200) |
| Chargement direct /page/inexistante | ✅ (code 404) |
| Page 404 : lien vers l’accueil du dépôt | ✅ (code /eportfolio/) |

## Liens vérifiés
| Lien | Vérification |
|---|---|
| Menu : 9 ancres internes (`#hero`, `#pitch`, `#projets`, `#carriere`, `#mobilites`, `#engagements`, `#activites`, `#cv`, `#contact`) | Cible existante et défilement vers la bonne section : ✅ |
| « Voir mon CV » (Carrière) → `#cv` | ✅ |
| « Voir le rôle modèle » (panneau de la carte) → `#plan-a`, `#plan-b`, `#plan-c` | ✅ |
| Téléchargements `documents/CV_Edgar_Lapouge_FR.pdf`, `documents/CV_Edgar_Lapouge_EN.pdf`, `documents/TIPE_horloge_glacon.pdf` | Fichier PDF réellement reçu par le navigateur sur les 8 formats : ✅ |
| `mailto:edgarpouge33@gmail.com` (bouton « Envoyer un mail ») | Adresse seule, sans objet ni corps, sans ouverture d’onglet vide : ✅ |
| LinkedIn `https://www.linkedin.com/in/edgar-lapouge-0ab779437` (2 liens) | Adresse identique à celle du portfolio d’origine, `rel="noopener"` : ✅. **Ouverture en ligne non testée** (pas d’accès Internet depuis l’environnement). |
| Présentation du TIPE (Google Slides) | Adresse transmise par Edgar, `rel="noopener"` : ✅. **Ouverture non testée** ; le partage doit être réglé sur « Tous les utilisateurs disposant du lien ». |
| Google Fonts (polices Inter et Lato) | **Non joignable depuis l’environnement** : les tests ont tourné avec les polices de secours (Helvetica, Arial). En ligne, les polices se chargeront normalement. |

## Fonctionnalités vérifiées
- Menu : défilement horizontal depuis le début sur petits écrans, lien actif souligné et ramené dans la zone visible, lien d’évitement « Aller au contenu ».
- Bascule français ↔ anglais (attribut `lang` du document, menu « Welcome », panneau, infobulles, rôles modèles).
- Vidéo de l’elevator speech (chargement, durée 3 min 11 s).
- Carte : un point par pays en vue globale, séparation des villes au zoom (Espagne, Italie), infobulle au survol et au toucher (toujours dans la carte), léger zoom au clic, informations à côté de la carte sur grand écran et en dessous sur téléphone, pincement à deux doigts, boutons +/−/recentrer.
- Galeries : miniatures, ouverture de la visionneuse sur la bonne photo, photo suivante, fermeture, focus déplacé sur « Fermer ».
- Activités : carrousel du surf, agrandissement des photos, illustrations judo, tennis et boxe.
- CV : onglets français/anglais, agrandissement de l’aperçu, téléchargements.
- Galeries de la Tanzanie (6 photos), du Maroc (2) et de l’Italie (5, dont le Colisée et le sous-marin de Cinecittà) ; phrase sur Cinecittà et le film *U-571* ; phrase sur les plantations de thé au Sri Lanka.
- Contrôle anti-doublon : aucune photo n’apparaît deux fois dans une galerie, ni dans deux galeries de voyage (la photo de surf au Panama figure volontairement aussi dans le carrousel surf, comme demandé le 29/10).
- Activités : carrousels football (3 photos) et surf (4 photos), photos du judo, de la boxe et du tennis.
- Bloc `PHOTOS_AJOUTEES` de `js/main.js` : testé avec deux photos d’essai (Tanzanie et Rome), les photos s’affichent et les emplacements disparaissent.

## Contrôles d’accessibilité
| Contrôle | Résultat |
|---|---|
| Contraste du texte (niveau AA : 4,5:1, 3:1 pour les grands textes), environ 201 textes mesurés par format | ✅ après corrections. Les textes posés sur une photo ne sont pas mesurables automatiquement (aucun dans la version finale) |
| Hiérarchie des titres (h1 → h2 → h3 → h4, sans saut) | ✅ |
| Attribut `alt` sur toutes les images (vide pour les images décoratives) | ✅ |
| Intitulé accessible pour tous les boutons et liens | ✅ |
| Navigation au clavier : lien d’évitement, focus visible, points de la carte accessibles avec Tab et Entrée | ✅ (les commandes internes de la vidéo ont le contour natif du navigateur) |
| Cibles tactiles d’au moins 24 × 24 px (hors liens dans le texte) | ✅ |
| Texte d’au moins 12 px | ✅ |
| Repères de structure : `header`, `nav`, `main`, `footer`, un seul `h1` | ✅ |
| Identifiants en double, liens sans `href`, boutons dans des liens, boutons sans `type` | Aucun ✅ |
| Animations réduites si l’utilisateur l’a demandé (`prefers-reduced-motion`) | Présent dans le code (non testé automatiquement) |

## Erreurs trouvées et corrections réalisées
| Problème trouvé | Correction |
|---|---|
| Sur tablette et téléphone, le début du menu (Présentation, Elevator speech, Projets…) était **inaccessible** : il débordait à gauche sans possibilité de défilement | Menu aligné à gauche quand il déborde, à droite sinon ; défilement automatique vers la section active |
| Téléchargements dépendants du lecteur claude.ai : **ne fonctionnaient pas sur GitHub Pages** | Vrais liens vers les PDF (attribut `download`), fichiers placés dans `documents/` |
| Toutes les images et les PDF étaient intégrés dans `index.html` (8 Mo) | Fichiers séparés aux noms descriptifs ; `index.html` ne pèse plus que 0,4 Mo |
| CSS et JavaScript mélangés au HTML | `css/style.css` et `js/main.js` séparés |
| Contrastes insuffisants : orange sur blanc (3,0:1), gris clair (3,4:1), boutons orange à texte blanc (3,3:1) | Teintes plus foncées pour les textes et les fonds de boutons (≥ 4,5:1), sans changer l’orange de la marque ailleurs |
| Étiquettes « Formation », « Expérience », « Rôle modèle » à 11,2 px | Passées à 12 px |
| Titres « PROFIL », « Soft skills », « Langage », « Outils » en h4 directement sous un h2 | Passés en h3 |
| Pas de `main`, pas de lien d’évitement, menu sans libellé | Structure `header` / `nav` / `main` / `footer`, lien « Aller au contenu », libellés traduits |
| Visionneuse : focus non géré, libellés en anglais sur le site français | Focus sur « Fermer » à l’ouverture puis rendu à la fermeture, libellés traduits |
| Lien mail ouvrant un onglet vide (`target="_blank"`) | Supprimé |
| Pas de description, pas d’icône d’onglet, titre peu explicite | Balises `description`, Open Graph, `theme-color`, icône SVG, titre plus clair |
| `padding` du menu qui annulait la marge de sécurité des iPhone à encoche | Corrigé (`safe-area-inset`) |
| 69 règles CSS et 2 constantes JavaScript inutilisées (anciennes versions de la carte) | Supprimées, avec vérification visuelle avant/après |
| Images de provenance inconnue ou tierce (Tanzanie, judo, tennis, boxe, Maroc, logo de football) | Retirées et remplacées par tes photos (voir `CREDITS-IMAGES.md`) |
| Photo de profil et graphique du TIPE déformés après l’ajout de leurs dimensions (erreur introduite pendant ce travail, repérée par les tests) | `height: auto` ajouté |
| Les deux icônes de la frise avaient été inversées lors de l’extraction (erreur introduite pendant ce travail, repérée par les tests) | Nommées d’après leur format réel |

## Éléments restant à confirmer
1. **Test sur de vrais appareils après publication** : iPhone (Safari), Android (Chrome) et Firefox sur ordinateur.
2. **Droits des images** : toutes les lignes « à confirmer » de `CREDITS-IMAGES.md`, notamment les personnes reconnaissables et les logos.
3. **Photo du Forum romain** facultative : la partie Rome est illustrée par le Colisée et Cinecittà.
4. **Nom de la seconde plantation de thé** au Sri Lanka : il ne figure dans aucun fichier fourni, il n’a donc pas été ajouté au texte.
5. **Partage de la présentation Google Slides** du TIPE à ouvrir à « Tous les utilisateurs disposant du lien ».
6. **Données personnelles** : numéro de téléphone (section Contact) et adresse postale (dans les CV PDF) seront publics. À conserver ou à retirer selon votre choix.
7. **Dates** : mises à jour selon tes indications (New York 2017, Barcelone 2016, Malaga et Nerja 2026, Rome 2015, Sicile 2017).
8. **Transcription de la vidéo** : il n’y a pas de sous-titres. Une transcription écrite améliorerait l’accessibilité et pourra être ajoutée si vous la rédigez.
