# Mettre l’e-portfolio en ligne avec GitHub Pages

Ce guide part de zéro : aucune connaissance de Git ou de GitHub n’est nécessaire. À la fin, vous aurez un **lien public cliquable** vers votre site, gratuit, que vous pourrez mettre sur votre CV ou LinkedIn.

**Ce qu’il vous faut** : le dossier `eportfolio-github` sur votre ordinateur, un navigateur (Chrome, Edge ou Firefox conseillés pour l’envoi des fichiers) et une adresse e-mail.

> **Avant de publier, pensez à vos données personnelles.** Le site sera visible par tout le monde. Il contient votre adresse e-mail et votre numéro de téléphone (section Contact), et vos CV en PDF contiennent aussi votre adresse postale. Si vous ne souhaitez pas les rendre publics, retirez-les avant la mise en ligne (voir le `README.md`, section « Modifier le contenu »).

---

## Partie 1 – Méthode simple, avec le site GitHub (recommandée)

### Étape 1 – Créer ou ouvrir un compte GitHub
1. Allez sur <https://github.com>.
2. Si vous avez déjà un compte, cliquez sur **Sign in** et connectez-vous.
3. Sinon, cliquez sur **Sign up**, saisissez votre e-mail, un mot de passe et un **nom d’utilisateur**. Ce nom apparaîtra dans l’adresse de votre site : choisissez-le simple et professionnel (par exemple `edgar-lapouge`).
4. Confirmez votre adresse e-mail avec le code reçu.

Dans la suite, `UTILISATEUR` désigne **votre** nom d’utilisateur GitHub.

### Étape 2 – Créer un dépôt public
Un « dépôt » (*repository*) est un dossier en ligne qui contiendra votre site.
1. En haut à droite de GitHub, cliquez sur le **+**, puis sur **New repository**.
2. Remplissez le formulaire comme indiqué aux étapes 3 et 4.

### Étape 3 – Choisir le nom du dépôt
- Dans **Repository name**, tapez par exemple `eportfolio`.
- Utilisez des minuscules et des tirets, sans espace ni accent : le nom fera partie de l’adresse du site.
- Votre site sera alors disponible à l’adresse `https://UTILISATEUR.github.io/eportfolio/`.

### Étape 4 – Ne rien ajouter d’autre à la création
- Cochez **Public** (obligatoire pour GitHub Pages avec un compte gratuit).
- **Ne cochez pas** « Add a README file », **ne choisissez pas** de `.gitignore` ni de licence : le dossier contient déjà ces fichiers, et des fichiers en double créeraient des conflits.
- Cliquez sur **Create repository**.

### Étape 5 – Importer le contenu du dossier `eportfolio-github`
1. Sur la page du dépôt vide, cliquez sur le lien **uploading an existing file**. Vous pouvez aussi passer par **Add file → Upload files**.
2. Sur votre ordinateur, **ouvrez** le dossier `eportfolio-github` et sélectionnez **tout ce qu’il contient** (`Ctrl` + `A` sous Windows, `Cmd` + `A` sur Mac) : `index.html`, `404.html`, les dossiers `css`, `js`, `images`, `documents`, `videos` et les fichiers `.md`.
3. **Glissez-déposez** cette sélection dans la zone d’envoi de GitHub. Les sous-dossiers sont conservés.

⚠️ **Ne glissez pas le dossier `eportfolio-github` lui-même**, mais son **contenu**. Sinon le site se retrouverait dans un sous-dossier et l’adresse afficherait une erreur 404.

**Fichiers cachés `.nojekyll` et `.gitignore`** : leur nom commence par un point, et ils sont souvent invisibles sur Mac.
- Sur Mac, appuyez sur `Cmd` + `Maj` + `.` dans le Finder pour les afficher, puis ajoutez-les à la sélection.
- S’ils ne passent pas, ce n’est pas bloquant : `.gitignore` ne sert qu’aux envois en ligne de commande, et `.nojekyll` n’est pas indispensable pour ce site. Pour l’ajouter quand même : **Add file → Create new file**, tapez `.nojekyll` comme nom, laissez le contenu vide, puis **Commit changes**.

**Limites de l’envoi par le navigateur** : 100 fichiers et 25 Mo par fichier à chaque envoi. Le dossier compte environ 80 fichiers et le plus gros (la vidéo) pèse 7,5 Mo : un seul envoi suffit. Si GitHub refuse, envoyez d’abord le dossier `images`, puis le reste.

### Étape 6 – Vérifier que `index.html` est à la racine
Une fois l’envoi terminé (la liste des fichiers apparaît sous la zone de dépôt), vérifiez que la liste montre directement `index.html`, `404.html`, `css`, `js`, `images`… et **non** un seul dossier `eportfolio-github`.

### Étape 7 – Valider l’importation
1. En bas de la page, dans **Commit changes**, laissez le message proposé ou écrivez « Publication initiale de mon e-portfolio ».
2. Vérifiez que **Commit directly to the main branch** est sélectionné.
3. Cliquez sur **Commit changes** et attendez la fin du chargement : la vidéo peut prendre quelques secondes.
4. Sur la page d’accueil du dépôt, `index.html` doit apparaître dans la liste des fichiers.

### Étape 8 – Ouvrir `Settings`
En haut de la page du dépôt, cliquez sur l’onglet **Settings** (icône d’engrenage).

### Étape 9 – Ouvrir `Pages`
Dans le menu de gauche, rubrique **Code and automation**, cliquez sur **Pages**.

### Étape 10 – Choisir le déploiement depuis une branche
Dans **Build and deployment**, à la ligne **Source**, choisissez **Deploy from a branch**.

### Étape 11 – Sélectionner la branche `main` et le dossier racine
Dans **Branch** :
- premier menu : **main** ;
- second menu : **/ (root)**, car `index.html` est à la racine du dépôt.

### Étape 12 – Enregistrer
Cliquez sur **Save**. GitHub prépare le site (une à trois minutes en général). Vous pouvez suivre l’avancement dans l’onglet **Actions** du dépôt : une coche verte indique que la publication est terminée.

### Étape 13 – Récupérer l’adresse publique
Rechargez la page **Settings → Pages**. En haut apparaît **« Your site is live at … »**, suivi d’un bouton **Visit site**. Cette adresse est votre lien public.

### Étape 14 – Vérifier le site comme un visiteur
1. **Fenêtre privée** sur ordinateur (`Ctrl` + `Maj` + `N` dans Chrome) : collez l’adresse et parcourez tout le site (menu, vidéo, carte, photos, téléchargements, bouton EN).
2. **Sur votre téléphone** : ouvrez l’adresse en 4G, sans Wi-Fi, pour être dans les conditions d’un recruteur. Touchez une photo, la carte, les boutons de téléchargement.
3. Si quelque chose ne va pas, consultez la partie « Problèmes fréquents » plus bas.

### Étape 15 – Comprendre l’adresse du site
Pour un dépôt classique, l’adresse suit la forme :

```
https://UTILISATEUR.github.io/NOM-DU-DEPOT/
```

Par exemple, avec un dépôt nommé `eportfolio`, elle devient `https://UTILISATEUR.github.io/eportfolio/`, où `UTILISATEUR` est **votre** nom d’utilisateur GitHub.

*Option* : si vous nommez le dépôt exactement `UTILISATEUR.github.io`, l’adresse devient plus courte, `https://UTILISATEUR.github.io/`. Les deux fonctionnent avec ce site, car tous ses liens sont relatifs.

### Étape 16 – Corriger et republier une modification
1. Modifiez le fichier sur votre ordinateur (par exemple une phrase dans `index.html`), puis vérifiez le résultat en local (voir `README.md`).
2. Sur GitHub, ouvrez votre dépôt, puis **Add file → Upload files**.
3. Glissez le fichier modifié **en respectant son dossier**. Pour un fichier situé dans un sous-dossier (par exemple `js/main.js`), ouvrez d’abord ce dossier sur GitHub en cliquant dessus, puis faites **Add file → Upload files** depuis ce dossier.
4. Un fichier du même nom est **remplacé**. Validez avec **Commit changes**.
5. Attendez une à deux minutes, puis rechargez le site avec `Ctrl` + `F5` (`Cmd` + `Maj` + `R` sur Mac) pour vider le cache.

Pour une petite correction de texte, vous pouvez aussi modifier directement sur GitHub : ouvrez le fichier, cliquez sur l’icône **crayon** (*Edit this file*), faites la modification, puis **Commit changes**.

---

## Partie 2 – Méthode facultative, en ligne de commande

À utiliser seulement si vous voulez apprendre Git. Il faut d’abord installer Git (<https://git-scm.com>), puis créer le dépôt vide sur GitHub comme aux étapes 2 à 4.

Ouvrez un terminal **dans le dossier `eportfolio-github`**, puis tapez ces commandes une par une, en remplaçant `UTILISATEUR` et `NOM-DU-DEPOT` :

```bash
git init
git add .
git commit -m "Publication initiale de mon e-portfolio"
git branch -M main
git remote add origin https://github.com/UTILISATEUR/NOM-DU-DEPOT.git
git push -u origin main
```

Ce que fait chaque commande :
- `git init` : transforme le dossier en dépôt Git local.
- `git add .` : sélectionne tous les fichiers. Ceux listés dans `.gitignore` sont exclus.
- `git commit -m "…"` : enregistre cette version avec un message.
- `git branch -M main` : nomme la branche principale `main`.
- `git remote add origin …` : relie le dossier à votre dépôt GitHub.
- `git push -u origin main` : envoie les fichiers sur GitHub.

Lors du `git push`, GitHub demande de vous identifier. Le mot de passe du compte n’est **pas** accepté : utilisez un **jeton d’accès personnel**, à créer dans *Settings → Developer settings → Personal access tokens*, ou bien l’application **GitHub Desktop**, qui gère la connexion pour vous.

Activez ensuite GitHub Pages comme aux étapes 8 à 13.

**Pour publier une modification ensuite** :

```bash
git add .
git commit -m "Description courte de la modification"
git push
```

---

## Problèmes fréquents

| Problème | Cause probable | Solution |
|---|---|---|
| Erreur 404 « There isn’t a GitHub Pages site here » | Publication pas encore terminée, ou `index.html` pas à la racine | Attendez 3 minutes, vérifiez l’onglet **Actions**, puis vérifiez l’étape 6 |
| Le site s’affiche sans mise en forme ni images | Dossiers `css`, `js` ou `images` non envoyés, ou placés dans un sous-dossier | Vérifiez que ces dossiers sont à la racine du dépôt |
| Une image ne s’affiche pas | Nom de fichier différent (majuscules, accents, extension `.JPG` au lieu de `.jpg`) | Renommez le fichier exactement comme dans le code |
| L’ancienne version s’affiche encore | Cache du navigateur | `Ctrl` + `F5` (Windows) ou `Cmd` + `Maj` + `R` (Mac) |
| La vidéo ne se lance pas | Fichier `videos/elevator-speech.mp4` absent | Renvoyez le dossier `videos` |
| GitHub refuse l’envoi | Plus de 100 fichiers ou un fichier de plus de 25 Mo | Envoyez en plusieurs fois (d’abord `images`) |
| Le bouton « Envoyer un mail » ne fait rien | Aucune application de messagerie configurée sur l’appareil du visiteur | Normal : l’adresse reste affichée et le bouton « Copier l’adresse » est là pour ça |
