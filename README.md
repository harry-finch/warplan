# Visualisation des Adresses sur OpenStreetMap

Ce projet est une application Web interactive permettant de visualiser des adresses sur une carte OpenStreetMap. Les utilisateurs peuvent saisir plusieurs adresses, visualiser leurs emplacements sur la carte, et afficher les limites administratives des villes lorsqu'elles sont reconnues.

![Screenshot](./screenshot.png "Screenshot")

## Fonctionnalités principales

1. **Ajout d'adresses** :
   - Les utilisateurs peuvent ajouter des champs pour saisir plusieurs adresses.
   - Un bouton "+" permet d'ajouter dynamiquement des champs supplémentaires.

2. **Affichage des adresses sur la carte** :
   - Les adresses sont localisées via l'API Nominatim.
   - Les marqueurs sont affichés sur la carte aux emplacements correspondants.

3. **Affichage des limites administratives** :
   - Si une adresse correspond à une ville ou une autre zone administrative, ses limites sont récupérées via Overpass API et affichées sous forme de polygones.

4. **Réinitialisation de la carte** :
   - Supprime tous les marqueurs et polygones, et réinitialise la vue de la carte à un état par défaut centré sur Paris.

5. **Interface utilisateur intuitive** :
   - Boutons ergonomiques avec des styles clairs pour ajouter ou supprimer des adresses.
   - Affichage des polygones et marqueurs avec des couleurs distinctes.

## Technologies utilisées

- **HTML/CSS** : Interface utilisateur stylée avec une mise en page responsive.
- **JavaScript** : Gestion dynamique des adresses, interaction avec les APIs, et manipulation de la carte.
- **Leaflet** : Bibliothèque de cartographie légère pour afficher et manipuler la carte.
- **API Nominatim** : Service de géocodage pour convertir des adresses en coordonnées GPS.
- **API Overpass** : Utilisée pour récupérer les limites géographiques des zones administratives.

## Installation

1. Clonez ce dépôt :
   ```bash
   git clone https://github.com/votre-repo/visualisation-adresses.git
   ```

2. Naviguez dans le dossier du projet :
   ```bash
   cd visualisation-adresses
   ```

3. Ouvrez le fichier `index.html` dans votre navigateur Web préféré.

## Utilisation

1. Entrez une ou plusieurs adresses dans les champs prévus à cet effet.
2. Cliquez sur le bouton "Afficher sur la carte" pour visualiser les adresses.
3. Les zones administratives des villes sont affichées en polygones bleus.
4. Cliquez sur "Réinitialiser la carte" pour tout effacer et revenir à l'état initial.

## Dépendances

- [Leaflet](https://leafletjs.com/) : Bibliothèque de cartographie.
- [Nominatim API](https://nominatim.org/) : API pour la géolocalisation.
- [Overpass API](https://overpass-api.de/) : API pour les données géographiques avancées d'OpenStreetMap.

## Personnalisation

- Vous pouvez modifier le style des polygones et marqueurs dans la section JavaScript :
  ```javascript
  const polyline = L.polyline(coordinates, {
      color: "blue",
      weight: 2,
      fillOpacity: 0.4,
  }).addTo(map);
  ```

- Le point central par défaut de la carte peut être modifié ici :
  ```javascript
  map.setView([48.8566, 2.3522], 5); // Centré sur Paris
  ```

## Limitations

- Les performances peuvent être affectées pour un grand nombre d'adresses ou de polygones complexes.
- Les résultats dépendent de la qualité des données disponibles dans OpenStreetMap.
- L'API Overpass peut être lente ou temporairement indisponible en cas de surcharge.

## Contribuer

Les contributions sont les bienvenues !

1. Forkez le projet.
2. Créez une branche pour votre fonctionnalité ou correction de bug :
   ```bash
   git checkout -b feature/ma-fonctionnalite
   ```
3. Effectuez vos modifications et poussez-les :
   ```bash
   git commit -m "Ajout d'une fonctionnalité"
   git push origin feature/ma-fonctionnalite
   ```
4. Soumettez une pull request.

## Licence

Ce projet est sous licence MIT. Consultez le fichier [LICENSE](LICENSE) pour plus de détails.

