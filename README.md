# mas-bom

Central versions for MAS Spring Boot applications (microservices) and libraries that need Spring (mas-core).
It imports the Spring Boot BOM, so all of them use the same Spring Boot version.

Not meant for mas-autotests, which manages its own library versions.

## Usage

Spring Boot application:
```gradle
dependencies {
    implementation enforcedPlatform('pl.es8it.mas.bom:mas-bom:1.0.0')
}
```

Library that must not pass the BOM on to its consumers:
```gradle
dependencies {
    compileOnly enforcedPlatform('pl.es8it.mas.bom:mas-bom:1.0.0')
}
```

## Publish
```bash
./gradlew publishToMavenLocal
```
