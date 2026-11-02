# Navigateur web Android

Navigateur web minimaliste pour Android, développé en Java dans le cadre d'un travail pratique au Cégep de Granby (2025).

L'application repose sur un `WebView` et reproduit les fonctions de base d'un navigateur : barre d'adresse, navigation dans l'historique, page d'accueil personnalisable et ouverture des liens non Web dans l'application appropriée.

## Fonctionnalités

- **Barre d'adresse** : saisir une URL et lancer la recherche avec le bouton de navigation ou la touche Entrée du clavier. Le schéma `https://` est ajouté automatiquement s'il est absent.
- **Liens non Web** : les schémas autres que `http`/`https` (`mailto:`, `tel:`, `sms:`, etc.) sont transmis au système via un `Intent`, pour ouvrir par exemple l'application de messagerie. Un message s'affiche si aucune application ne peut les gérer.
- **Précédent / Suivant** : navigation dans l'historique du `WebView`. Les boutons sont désactivés (et grisés) lorsqu'aucune action n'est possible.
- **Page d'accueil** : retour à la page d'accueil et définition de la page courante comme nouvelle page d'accueil.
- **Progression du chargement** : barre de progression affichée pendant le chargement de la page.
- **Clavier** : fermeture automatique du clavier après une recherche ou lorsque la barre d'adresse perd le focus.

## Technologies

- Java
- Android SDK (min SDK 24, cible SDK 35)
- `WebView`, `WebViewClient`, `WebChromeClient`
- AndroidX (AppCompat, ConstraintLayout, Material Components)
- Gradle (Kotlin DSL)

## Structure

```
app/src/main/
├── java/com/example/tp2_android/MainActivity.java   # Logique du navigateur
├── res/layout/activity_main.xml                      # Interface (barre d'adresse, boutons, WebView)
├── res/drawable*/                                    # Icônes des boutons (actifs et désactivés)
└── AndroidManifest.xml                               # Permission INTERNET
```

## Lancer le projet

1. Cloner le dépôt :
   ```bash
   git clone https://github.com/Yacine3111/Android-web-browser.git
   ```
2. Ouvrir le dossier dans **Android Studio**.
3. Laisser Gradle synchroniser les dépendances.
4. Lancer l'application sur un émulateur ou un appareil Android (API 24 ou plus).

Ou en ligne de commande :

```bash
./gradlew installDebug
```

## Auteur

Yacine Bourezak — [GitHub](https://github.com/Yacine3111) · [LinkedIn](https://www.linkedin.com/in/yacine-bourezak)
