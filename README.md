# Spring REST Service

Service REST « Hello, World » construit avec **Spring Boot 4.0.9** et **Java 17**.
Il expose un point d'entrée HTTP GET qui renvoie une salutation au format JSON.

> Ce dépôt est basé sur le guide officiel [Building a RESTful Web Service](https://spring.io/guides/gs-rest-service).
> Voir [README.adoc](README.adoc) pour le contenu pédagogique complet.

## Fonctionnalités

- `GET /greeting` → `{"id":1,"content":"Hello, World!"}`
- `GET /greeting?name=User` → `{"id":1,"content":"Hello, User!"}`
- L'`id` s'incrémente à chaque requête ; le `name` est optionnel (`World` par défaut).

## Structure du projet

| Dossier | Contenu |
|---|---|
| `initial/` | Projet de départ (squelette) — Maven et Gradle |
| `complete/` | Projet terminé et fonctionnel — Maven et Gradle |
| `initial-kotlin/` | Variante Kotlin du projet de départ |
| `complete-kotlin/` | Variante Kotlin du projet terminé |
| `test/` | Scripts de vérification du guide |

## Prérequis

- JDK 17 ou supérieur
- Maven (ou le wrapper `./mvnw` fourni)
- Gradle (ou le wrapper `./gradlew` fourni)

## Lancer l'application

Avec Maven :

```bash
cd complete
./mvnw spring-boot:run
```

Avec Gradle :

```bash
cd complete
./gradlew bootRun
```

L'application démarre sur <http://localhost:8080>.

## Tester le service

```bash
curl http://localhost:8080/greeting
# {"id":1,"content":"Hello, World!"}

curl "http://localhost:8080/greeting?name=User"
# {"id":2,"content":"Hello, User!"}
```

## Tests

```bash
cd complete
./mvnw test      # ou ./gradlew test
```

## Licence

Le contenu du guide est publié sous licence Apache 2.0 — voir [LICENSE.txt](LICENSE.txt).
