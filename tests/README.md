# Frontend

Dans le répertoire frontend, utiliser

```
ng test
```

pour exécuter les tests.

Pour rouler le frontend

```
ng serve
```

# Backend

Vous devez installer le firebase cli.

```
npm install -g firebase-tools
```

Puis dans le répertoire backend

```
firebase init
```

Pour installer

- firestore
- emulator (firestore)

Ensuite, copier votre clé firebase dans le fichier firebase-key.json à la racine du répertoire backend.

Ajuster l'id de votre projet firebase dans firebase.properties.
Assurez-vous que le port de l'émulateur est 8181 (firebase.json).

Vous pouvez rouler l'émulator avec

Pour exécuter les tests

```
firebase emulators:exec "./mvnw integration-test"
```

Pour rouler le backend

```
./mvnw clean spring-boot:run
```

Pour rouler les tests en debug avec Visual Studio Code, vous pouvez rouler l'émulateur avec

```
firebase emulators:start
```

Vous devez configurer Visual Studio Code (chercher java.test.config dans les settings) pour qu'il ajoute dans les variables d'environnement:

```
FIRESTORE_EMULATOR_HOST = localhost:8181
```

Celà devrait ressembler au json suivant dans votre settings.json.

```
{
  ...
  "java.test.config": {
    "env": {
      "FIRESTORE_EMULATOR_HOST": "localhost:8181"
    }
  }
  ...
}

```

## Auteurs

- Danny Jered Okandze
- David Adjele
- Richard Tshimanga
