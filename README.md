# Better Calendar Workshop App

## Introduction

L'**application Better Calendar Workshop** est une application Android simple qui utilise un `WebView` pour afficher une page web personnalisée. L'application est conçue pour charger le site web "https://workshop.romain-igounet.fr/" directement dans l'application, offrant ainsi une expérience utilisateur fluide sans avoir besoin d'ouvrir un navigateur externe.

Cette application utilise le SDK Android ainsi que Kotlin pour son implémentation, garantissant la compatibilité à partir de l'API niveau 21 (Android 5.0 Lollipop) jusqu'aux versions les plus récentes du SDK Android.

## Dépôt de l'application Web

Le dépôt GitHub pour l'application Web est disponible à l'adresse suivante :

[Better Calendar Web Repo](https://github.com/BlaCkMatiK/better_calendar)

## Fonctionnalités

- **Intégration du WebView** : La fonctionnalité principale est la capacité à charger et afficher du contenu web directement dans l'application en utilisant le `WebView` d'Android.
- **Support JavaScript** : Le JavaScript est activé dans les paramètres du `WebView` pour permettre des interactions dynamiques avec la page web.
- **Options de menu dans la barre d'outils** : L'application inclut un menu avec une action "Home" qui permet à l'utilisateur de recharger la page d'accueil du site.
- **Configuration de la sécurité réseau** : L'application est configurée pour autoriser le trafic en texte clair pour des domaines spécifiques (par exemple, "nextcloud.romain-igounet.fr").

## Prise en main

### Prérequis

- **Android Studio** : Dernière version
- **Kotlin** : Intégré à Android Studio
- **SDK Android** : Le SDK cible est 34, avec un SDK minimum de 21.

### Installation

1. Clonez le dépôt sur votre machine locale :
   ```bash
   git clone https://github.com/your-repository/bettercalendar.git
   ```

2. Ouvrez le projet dans Android Studio.

3. Synchronisez le projet avec les fichiers Gradle.

4. Connectez un appareil Android ou lancez un émulateur.

5. Exécutez l'application en cliquant sur le bouton "Run" dans Android Studio.

### Structure du projet

- **MainActivity.kt** : Ce fichier contient la logique principale de l'application. Il initialise le `WebView` et gère le chargement de l'URL spécifiée.
  
- **Fichier Manifest** : Le fichier `AndroidManifest.xml` configure les permissions (comme `INTERNET`), le thème de l'application et l'activité de lancement.
  
- **Configuration de la sécurité réseau** : Le fichier `network-security-config.xml` permet le trafic en texte clair pour des domaines spécifiques.

- **Layouts et ressources** : Tous les composants de l'interface utilisateur, y compris l'icône de l'application, les fichiers de mise en page et les chaînes de caractères, sont stockés dans `res/`.

### Permissions

L'application nécessite les permissions suivantes :
- **INTERNET** : Pour charger du contenu web dans le `WebView`.

## Utilisation

- **Bouton Home** : Vous pouvez appuyer sur le bouton "Home" dans la barre d'outils pour recharger la page principale du site web ("https://workshop.romain-igounet.fr/").
  
- **Navigation** : L'application permet la navigation à l'intérieur du contenu web chargé, comme dans un navigateur.

## Dépendances

Le projet utilise plusieurs bibliothèques AndroidX et Jetpack Compose pour l'interface utilisateur et les tests :
- `androidx.core:core-ktx`
- `androidx.lifecycle:lifecycle-runtime-ktx`
- `androidx.activity:activity-compose`
- `androidx.appcompat:appcompat`
- `androidx.constraintlayout:constraintlayout`
- `androidx.compose:compose-bom`
- `androidx.material3`

## Compilation et publication

L'application a deux types de compilation :
- **Debug** : Utilisé pendant le développement avec des outils de journalisation et de débogage supplémentaires.
- **Release** : Optimisé pour la production avec une configuration Proguard pour la minification du code.
