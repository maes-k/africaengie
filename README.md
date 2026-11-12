# AfricaEngie — Site multipage

Version HTML, CSS et JavaScript pur, prête pour GitHub Pages.
Aucune installation npm, base de données ou compilation n’est nécessaire.

## Fichiers

- `index.html` : accueil.
- `solutions.html` : solutions, cas d’usage et comparaison.
- `approche.html` : accompagnement et préparation du projet.
- `simulateur.html` : calcul indicatif des consommations.
- `contact.html` : coordonnées et préparation d’une demande WhatsApp.
- `style.css` : styles communs et adaptations mobiles.
- `app.js` : menu, simulateur, onglets et formulaire.
- `assets/` : logo et images WebP optimisées, inclus dans l’archive.
- `.nojekyll` : publication du site statique sans traitement Jekyll.

## Tester sur votre ordinateur

1. Extraire toute l’archive dans un dossier.
2. Ouvrir ce dossier dans VS Code.
3. Avec l’extension Live Server, clic droit sur `index.html`, puis « Open with Live Server ».
4. Naviguer entre les cinq pages et tester le simulateur.

Il n’y a pas de serveur Node à démarrer pour cette version.

## Publier sur GitHub, sans terminal

1. Se connecter au compte GitHub `maes-k`.
2. Créer un dépôt PUBLIC nommé `africaengie`.
3. Ajouter les fichiers extraits et le dossier `assets` avec « Add file » > « Upload files ».
4. IMPORTANT : `index.html` doit se trouver directement à la racine du dépôt, au même niveau que `style.css`, `app.js` et les autres pages. Ne pas envoyer uniquement le ZIP, ni placer tout le site dans un sous-dossier supplémentaire.
5. Enregistrer avec « Commit changes ».
6. Ouvrir « Settings » > « Pages ».
7. Dans « Build and deployment », choisir « Deploy from a branch ».
8. Sélectionner la branche `main`, puis le dossier `/(root)`, et cliquer sur « Save ».
9. Attendre la fin de la publication. GitHub affichera le lien effectif et un bouton « Visit site ».

Si le dépôt est bien `maes-k/africaengie`, le lien attendu est :
https://maes-k.github.io/africaengie/
Ce lien ne sera actif qu’après la publication effective dans votre compte.

Le site utilise des chemins relatifs : ses images et ses liens conviennent à ce sous-dossier GitHub Pages.

## Alternative : publier avec Git dans PowerShell

Créer d’abord le dépôt public `africaengie` sur GitHub, SANS initialiser de README ni d’autres fichiers.
Ouvrir le terminal dans le dossier qui contient directement `index.html`, puis exécuter :

```powershell
git init
git add .
git commit -m "Publication initiale du site AfricaEngie"
git branch -M main
git remote add origin https://github.com/maes-k/africaengie.git
git push -u origin main
```

Ces commandes sont destinées à un dossier neuf. Dans un dépôt Git existant, vérifier d’abord `git status` et `git remote -v`.
Activer ensuite Pages dans Settings comme indiqué ci-dessus.

## Fonctionnement du contact

Le formulaire prépare un message sur WhatsApp vers +225 07 16 77 21 15.
Le visiteur doit vérifier et envoyer lui-même ce message dans WhatsApp.
Aucune demande n’est stockée dans une base de données et aucun e-mail n’est envoyé automatiquement.
L’e-mail de contact est : africaengieci@gmail.com.

Le simulateur calcule une consommation indicative en kWh/jour et une projection sur 30 jours d’usage identique. Il ne dimensionne pas automatiquement les panneaux, les batteries ou l’onduleur.
La transmission de l’estimation entre les pages utilise le stockage de session du navigateur dans le même onglet.

## Personnaliser

- Textes : modifier les pages HTML concernées.
- Couleurs, typographies et espacements : modifier `style.css`.
- Calculs et comportement du formulaire : modifier `app.js`.
- Téléphone : rechercher `2250716772115` dans les fichiers avant remplacement.
- Images : conserver leur nom ou mettre à jour les attributs `src`, `srcset` et les préchargements concernés.

## Images et polices

Les images sont intégrées localement au dossier `assets`, sans dépendance à un serveur d’images externe.
Les illustrations de batteries et de pompage ont été générées ; elles ne constituent pas des photographies de chantiers réels AfricaEngie.
Le logo provient du fichier officiel fourni.
Photographies solaires d’illustration utilisées :
- https://images.unsplash.com/photo-1509391366360-2e959784a276
- https://images.unsplash.com/photo-1497440001374-f26997328c1b

Les polices DM Sans et Manrope sont chargées via Google Fonts avec des polices de remplacement disponibles.

## En cas de page vide ou d’erreur 404

- Vérifier que le fichier s’appelle exactement `index.html`.
- Vérifier qu’il est à la racine et que le dossier Pages sélectionné est `/(root)`.
- Vérifier la publication dans l’onglet « Actions » du dépôt.
- Conserver le dossier `assets` et tous les noms de fichiers, y compris les minuscules.
- Actualiser avec Ctrl + F5 après une mise à jour.

Documentation officielle :
https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site

## Mise à jour de lisibilité — 12 novembre 2026

Les petits textes ont été agrandis sur les cinq pages. Le menu se replie également sur tablette pour conserver de l’espace. Les champs de formulaire utilisent une police de 16 px.
Pour mettre à jour votre site, remplacer les fichiers HTML, style.css et app.js par ceux de cette archive, puis envoyer les changements sur GitHub. Le dossier assets est inclus pour une installation complète.

Mise à jour : les textes précédemment à 14 px passent à 16 px sur les cinq pages.
