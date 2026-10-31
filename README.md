# E-portfolio d’Edgar Lapouge

Site personnel d’Edgar Lapouge, élève ingénieur à l’ENSEEIHT (Toulouse) en mécanique des fluides, énergétique et environnement. Il présente son elevator speech, ses projets d’ingénieur, son parcours, ses mobilités (voyages réalisés et mobilités envisagées), ses engagements, ses activités et son CV, en français et en anglais.

Le site est **statique** : de simples fichiers HTML, CSS et JavaScript, sans installation ni compilation. Il se publie tel quel sur GitHub Pages.

## Structure du dossier

```
eportfolio-github/
├── index.html              Page unique du site (toutes les sections)
├── 404.html                Page affichée si une adresse n’existe pas
├── css/
│   └── style.css           Mise en forme (couleurs, disposition, version mobile)
├── js/
│   └── main.js             Interactions : carte, galeries, traduction, menus…
├── images/
│   ├── profil/             Portrait et aperçu de la vidéo
│   ├── projets/            Graphiques du TIPE
│   ├── parcours/           Icônes de la frise « Formation et expériences »
│   ├── voyages/            Photos des voyages (version -lg grande, -sm miniature)
│   ├── activites/          Photos et illustrations des activités
│   ├── drapeaux/           Drapeaux des pays visités
│   ├── cv/                 Aperçus des CV
│   └── favicon.svg         Icône de l’onglet du navigateur
├── documents/              CV (français et anglais) et présentation du TIPE en PDF
├── videos/
│   └── elevator-speech.mp4 Vidéo de présentation
├── README.md               Ce fichier
├── CREDITS-IMAGES.md       Provenance et droits de chaque image
├── CHECKLIST-TESTS.md      Ce qui a été testé et les résultats
├── DEPLOIEMENT-GITHUB.md   Guide pas à pas pour mettre le site en ligne
├── .gitignore              Fichiers à ne pas envoyer sur GitHub
└── .nojekyll               Indique à GitHub Pages de publier les fichiers tels quels
```

## Technologies utilisées

- **HTML5, CSS3 et JavaScript** « natif » (aucun framework, aucune bibliothèque à installer).
- **Polices Inter et Lato** chargées depuis Google Fonts (si elles ne se chargent pas, le site utilise Helvetica ou Arial).
- Carte du monde dessinée en SVG directement dans `index.html`.
- Aucun serveur, aucune base de données, aucun formulaire : les téléchargements sont de simples liens vers les PDF, le bouton « Envoyer un mail » ouvre la messagerie de l’utilisateur.

## Ouvrir le site sur son ordinateur

**Méthode simple** : double-cliquez sur `index.html`. Le site s’ouvre dans votre navigateur.

**Méthode recommandée pour tester** (plus proche de la mise en ligne) : utilisez un petit serveur local.
1. Ouvrez un terminal dans le dossier `eportfolio-github` :
   - Windows : dans l’explorateur, ouvrez le dossier, cliquez dans la barre d’adresse, tapez `cmd` puis Entrée.
   - Mac : clic droit sur le dossier, puis « Nouveau terminal au dossier ».
2. Tapez `python -m http.server 8000` (ou `python3 -m http.server 8000` sur Mac), puis Entrée.
3. Ouvrez <http://localhost:8000> dans votre navigateur.
4. Pour arrêter le serveur, revenez au terminal et appuyez sur `Ctrl` + `C`.

Python est déjà installé sur Mac. Sous Windows, s’il manque, installez-le depuis <https://www.python.org> ou utilisez la méthode simple.

## Tester le site

La liste complète des contrôles se trouve dans `CHECKLIST-TESTS.md`. Avant chaque mise en ligne, vérifiez au minimum :
1. Le menu mène à chaque section, et le bouton EN/FR change la langue.
2. La vidéo de l’elevator speech se lance.
3. Dans « Mobilités » : la carte se zoome, un clic sur un point affiche les informations à côté (ou en dessous sur téléphone), les photos s’agrandissent.
4. Les boutons de téléchargement des CV et du TIPE ouvrent ou téléchargent le bon PDF.
5. Sur téléphone : rien ne dépasse de l’écran et les photos s’ouvrent au toucher.

Pour simuler un téléphone sur ordinateur : dans Chrome, appuyez sur `F12`, puis sur l’icône téléphone/tablette en haut à gauche du panneau.

## Modifier le contenu

Ouvrez les fichiers avec un éditeur de texte (par exemple **Visual Studio Code**, gratuit) et utilisez la recherche (`Ctrl` + `F`, ou `Cmd` + `F` sur Mac) pour trouver la phrase à changer.

| Ce que vous voulez modifier | Où le trouver |
|---|---|
| Présentation, projets, carrière, CV, contact | `index.html` |
| Textes des voyages, des activités, des engagements | `js/main.js` |
| Traductions anglaises | `js/main.js`, dans l’objet `D` : chaque ligne associe `"phrase française": "English sentence"` |
| Couleurs et mise en page | `css/style.css` (couleurs principales au début : `--s` vert, `--o` orange) |

**Important pour la traduction** : si vous modifiez une phrase française, modifiez aussi la même phrase dans l’objet `D` de `js/main.js` (à gauche des deux-points), sinon la version anglaise ne la retrouvera plus.

Gardez les guillemets, les virgules et les crochets tels quels : une virgule oubliée dans `js/main.js` peut bloquer toute la page. Après chaque modification, rechargez la page et vérifiez qu’elle fonctionne.

## Remplacer ou ajouter une image

1. **Préparez l’image** : JPEG, environ 1 600 px de large, moins de 500 Ko si possible. L’outil gratuit <https://squoosh.app> permet de la réduire sans installation.
2. **Nommez-la simplement** : en minuscules, sans espace ni accent (par exemple `italie-rome-forum-romain.jpg`). GitHub Pages distingue les majuscules : `Photo.JPG` et `photo.jpg` sont deux fichiers différents.
3. **Déposez-la** dans le bon dossier d’`images/`.
4. **Branchez-la** :
   - **Photo de voyage** (par exemple une photo du Forum romain) : en haut de `js/main.js`, dans la liste `PHOTOS_AJOUTEES`, retirez les deux barres `//` au début de l’exemple correspondant et adaptez le chemin et la légende. La photo s’ajoute à la galerie du pays.
   - **Autre image** (portrait, activité…) : remplacez simplement le fichier existant par un fichier **du même nom**, ou modifiez le chemin dans `index.html` / `js/main.js`.
5. **Complétez `CREDITS-IMAGES.md`** : source, auteur, licence et lien. N’utilisez jamais une image trouvée sur Internet sans avoir vérifié sa licence sur la page d’origine.

## Crédits des images

Tout est consigné dans `CREDITS-IMAGES.md`, avec le statut de chaque image (vérifié, à confirmer, à remplacer) et la liste des confirmations attendues.

## Publier et mettre à jour

Le guide complet, pas à pas, est dans `DEPLOIEMENT-GITHUB.md`. En résumé :
- **Première publication** : créer un dépôt public sur GitHub, y importer le **contenu** de ce dossier (pour que `index.html` soit à la racine du dépôt), puis activer GitHub Pages dans *Settings → Pages* (branche `main`, dossier `/ (root)`).
- **Mise à jour** : modifier le fichier sur votre ordinateur, puis le déposer à nouveau sur GitHub (*Add file → Upload files*) et valider. Le site se met à jour en une à deux minutes.
