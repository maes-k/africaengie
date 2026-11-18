# Référencement d’AfricaEngie — mise à jour du 13 novembre 2026

## Ce qui est intégré

- Titre et meta description spécifiques pour les cinq pages.
- Titres principaux plus explicites sur les pages intérieures.
- Texte d’accueil présentant les services et la zone d’intervention.
- Une URL canonique absolue par page.
- Accueil canonique : https://maes-k.github.io/africaengie/
- Liens vers l’accueil harmonisés vers `./`.
- Balises Open Graph et Twitter pour le partage.
- Données structurées JSON-LD : Organization, WebSite, WebPage et fil d’Ariane des pages intérieures.
- Fichier sitemap.xml avec les cinq URL canoniques.
- Police agrandie, bandeau supérieur supprimé et images optimisées conservés.

Les données de l’entreprise utilisent uniquement le nom, les coordonnées et la zone d’intervention déjà fournis. Aucun avis, note, chantier, qualification, adresse physique ou horaire n’a été inventé. Les données structurées ne garantissent pas un résultat enrichi dans Google.

## Mettre à jour le dépôt existant

1. Décompresser l’archive.
2. Copier son contenu dans le dossier du dépôt local, là où se trouve déjà index.html.
3. Remplacer les fichiers portant le même nom. Conserver le dossier .git existant.
4. Ajouter aussi sitemap.xml et ce guide à la racine du dépôt.
5. Dans le terminal du projet :

```bash
git status
git add .
git commit -m "Ajout du référencement naturel AfricaEngie"
git push
```

La configuration GitHub Pages existante ne nécessite pas de changement.
Vérifier la fin du déploiement dans l’onglet Actions de GitHub.

## Connecter Google Search Console : action manuelle restante

1. Ouvrir https://search.google.com/search-console/
2. Ajouter une propriété de type PRÉFIXE D’URL, avec l’adresse exacte :
   https://maes-k.github.io/africaengie/
3. Choisir la validation par balise HTML.
4. Copier la balise `google-site-verification` personnelle fournie par Google.
5. La coller dans le `<head>` de index.html, avant `</head>`.
6. Enregistrer, faire un commit et pousser sur GitHub ; attendre le déploiement.
7. Revenir dans Search Console puis cliquer sur Valider. Conserver cette balise ensuite.
8. Dans Sitemaps, soumettre l’adresse complète :
   https://maes-k.github.io/africaengie/sitemap.xml
9. Inspecter l’URL de l’accueil puis les pages principales et demander leur indexation si nécessaire.

Aucune balise de validation factice n’a été insérée. Cette étape demande le code propre à votre compte Google. L’archive n’effectue aucune validation ni soumission automatique.

## robots.txt et GitHub Pages

Le site se trouve dans le sous-chemin /africaengie/. Un robots.txt placé dans ce dépôt serait accessible à /africaengie/robots.txt : ce n’est pas l’emplacement reconnu pour les règles de robots.txt, qui se situe à la racine de l’hôte, /robots.txt.
Aucun robots.txt inutile n’a donc été ajouté à ce dossier. Soumettre directement le sitemap dans Search Console. Si un robots.txt existe à la racine de maes-k.github.io, vérifier qu’il ne bloque pas /africaengie/.

## Version principale et domaine futur

Toutes les URL SEO ciblent la version GitHub Pages publique. La balise canonique est un signal pour Google ; elle ne constitue pas une redirection.
Si le site passe sur un domaine officiel, mettre à jour les URL canoniques, le sitemap, les balises de partage et les identifiants/URL JSON-LD, puis préparer la migration et la nouvelle propriété Search Console.
L’aperçu de travail sur une autre adresse n’est pas mis à jour par cette archive. Le garder privé ou configurer sa non-indexation s’il est rendu public.

## Mesurer les progrès

Dans Search Console, suivre les pages indexées, les requêtes, les impressions, les clics et les erreurs. Le référencement se construit progressivement : aucune position ou date d’indexation n’est garantie.

## Contenus à compléter avec des informations réelles

- Photos de chantiers avec accord du client.
- Réalisations : localité, besoin, équipements et résultats vérifiés.
- Présentation de l’équipe et qualifications documentées.
- Adresse et horaires confirmés, si applicables.
- Fiche d’établissement Google renseignée avec exactitude.
- Pages dédiées aux principaux services lorsque du contenu détaillé est prêt.

## Documentation officielle

- https://developers.google.com/search/docs/fundamentals/seo-starter-guide?hl=fr
- https://developers.google.com/search/docs/crawling-indexing/sitemaps/build-sitemap?hl=fr
- https://developers.google.com/search/docs/crawling-indexing/consolidate-duplicate-urls?hl=fr
- https://support.google.com/webmasters/answer/34592?hl=fr
