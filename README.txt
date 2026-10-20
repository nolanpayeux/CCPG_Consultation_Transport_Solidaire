CCPG — Version consultation V1

Contenu : public/index.html, public/data/zonage.json,
public/data/isochrones/global.geojson

Déployer le dossier public/ sur un NOUVEAU projet Cloudflare Pages.
Ne pas remplacer le site administrateur.

Pour ajouter une commune ultérieurement :
1. déposer public/data/isochrones/<CODE_INSEE>.geojson
2. dans le dernier script de index.html, ajouter dans registry
   la correspondance 'CODE_INSEE':'/data/isochrones/CODE_INSEE.geojson'
3. activer l'option correspondante (le script de chargement le fait
   si vous appelez ccpgAjouterIsochrones(code,url)).
Les fichiers individuels ne sont pas encore disponibles.

La consultation des isochrones et du zonage ne consomme pas d'API ORS.
Le fond cartographique et le chargement des contours CCPG
utilisent toujours des services web externes.
