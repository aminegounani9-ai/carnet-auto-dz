# Carnet Auto DZ 🇩🇿

Application Android de gestion automobile avec interface française, icône dédiée et base SQLite embarquée. Le cœur de l'application fonctionne hors ligne : aucune connexion à un serveur n'est requise.

## Modules
- Tableau de bord et indicateurs
- Garage multi-véhicules : marque, modèle, année, matricule, VIN, carburant, kilométrage, moteur et couleur
- Carnet d'entretien : interventions, coûts, garage, pièces, prochain kilométrage et prochaine date
- Carburant : pleins, station, litres, prix, compteur
- Dépenses : catégories, paiement et montants en DZD
- Documents : assurance, contrôle technique, vignette, carte grise et dates d'expiration
- Rappels : échéance date/kilométrage et notifications locales
- Trajets : départ, destination, compteurs et distance
- Pièces : références, stock minimum, prix et fournisseur
- Rapports : indicateurs et export PDF
- Paramètres : sons, vibrations et notifications

## Technologies
- Expo SDK 54, React Native, TypeScript
- SQLite via expo-sqlite
- Notifications locales via expo-notifications
- Retour haptique, son d'interface et animations
- Export PDF via expo-print et expo-sharing

## Démarrer
```bash
npm install
npx expo start
```

## Générer un APK Android
```bash
npm install -g eas-cli
eas login
eas build --platform android --profile preview
```

Le profil `preview` dans `eas.json` est configuré pour produire un APK installable. Le workflow GitHub Actions vérifie le typage et l'export Android à chaque push.

## Données
Les données sont stockées dans `carnet-auto-dz.db` sur l'appareil. Les migrations ajoutent les nouvelles colonnes aux anciennes tables sans supprimer les enregistrements existants. Effectuer une sauvegarde avant de désinstaller l'application ou de changer de téléphone.
