# ReactNative: premiers pas

## Structure d'un projet ReactNative

Les projets ReactNative sont toujours composés de **deux dossiers de développement**, l'un pour iOS et l'autre pour Android. Vous trouverez également un dossier (node_modules) contenant l'ensemble des dépendances nécessaire à l'exécution de votre code.

* android
* ios
* node_modules
* .eslintrc
* .watchmanconfig
* **index.android.js**
* **index.ios.js**
* package.json


## Initialiser un projet

### Windows
___

#### Initialiser un projet sur Windows
* Se rendre dans le dossier de travail
* Entrer la commande suivante : `react-native init nom_du_projet`

#### Tester le projet via Android Studio
* Démarrer Android Studio
* Récupérer le projet créé à l'étape précédente et l'ouvrir
* Lors de la première ouverture d'Android Studio, vous obtenez un message d'erreur vous prévisant qu'il manque des plateformes pour l'exécution du code. Cliquez simplement sur le lien proposé.
* Créer ou utiliser un émulateur de périphérique mobile (Android Virtual Device) (voir ci-dessous)
* Démarrer l'émulateur
* `react-native run-android`

##### Création d'un périphérique mobile dans Android Studio (AVD)
* Tools > Android > AVD Manager
* Create Virtual Device
* Choisir un preset ou créer un périphérique soi-même
* S'assurer que la version d'Android utilisée est bien compatible avec ReactNative
* Une fois que la version d'Android est téléchargé, il ne vous reste plus qu'à la sélectionner (elle apparait en gras dans la liste)
* Next -> Finish

##### Ajout des variables d'environnement *
* Dans le menu démarrer, clic droit sur *Ordinateur* > Propriétés > Paramètres avancés > Variables d'environnement
* Nouvelle > Nom : JAVA_HOME /// Valeur : chemin_absolu_vers_le_dossier_Java_SDK_dans_votre_ordinateur
* Il vous faudra ensuite éditer la variable existante `Path` et y ajouter ceci C:\\chemin_absolu_vers ... AppData\Local\Android\sdk\plateform-tools
* Redémarrez votre invite de commande et rendez-vous dans à la racine dossier contenant votre projet


\* Si vous avez une variable JAVA_HOME, ne pas effectuer cette étape.


### Mac OS
___

### Initialiser un projet sur Mac OS
* Se rendre dans le dossier de travail
* Entrer la commande suivante : `react-native init nom_du_projet`


### Tester le projet via Xcode (simulateur iOS)
* Démarrer Xcode
* Choisir un environnement de test (iPhone x / iPad x)
* Ouvrir le terminal et se rendre dans le dossier du projet initialisé précedemment.
* `react-native run-ios`

