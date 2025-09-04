# Board (Kanban) - Java + Gradle

Um projeto simples de quadro Kanban com JDBC e Liquibase.

## Requisitos
- Java 17+
- Gradle (wrapper incluso: `gradlew`/`gradlew.bat`)
- MySQL em execução (ou adapte as credenciais em `src/main/resources/liquibase.properties`)

## Como rodar
1. Compile:
   ```bash
   ./gradlew build
   ```
2. Execute (se houver `Main`):
   ```bash
   ./gradlew run
   ```

## Migrações (Liquibase)
- Arquivo de propriedades: `src/main/resources/liquibase.properties`
- Changelog principal: `src/main/resources/db/changelog/db.changelog-master.yml`
- Para aplicar migrações, rode a aplicação (o projeto configura a estratégia via código) ou use o CLI do Liquibase.

## Comandos úteis
- Formatar código (Spotless):
  ```bash
  ./gradlew spotlessApply
  ```
- Testes (quando houver):
  ```bash
  ./gradlew test
  ```

## Estrutura
- `src/main/java/br/com/dio/` — código fonte (DTOs, DAOs, Services, UI)
- `src/main/resources/db/` — changelogs do Liquibase
- `build.gradle.kts` — configuração Gradle

## Notas
- Lombok é usado para reduzir boilerplate (getters/setters). Configure sua IDE para suportar Lombok.
- Logs e artefatos de build são ignorados via `.gitignore`.
