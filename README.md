# Carnet Auto DZ 🇩🇿

Application Android de suivi automobile pour l'Algérie. Interface française, base SQLite locale et fonctionnement hors ligne.

## Technologies
- Expo + React Native + TypeScript
- SQLite via expo-sqlite
- Identifiant Android : `dz.carnetauto.app`

## Démarrer
```bash
npm install
npx expo start
```

## Générer un APK installable
```bash
npm install -g eas-cli
eas login
eas build --platform android --profile preview
```

Le profil preview est configuré pour produire un APK. Les données des véhicules, entretiens, carburant et dépenses sont stockées localement sur le téléphone, sans Supabase.
