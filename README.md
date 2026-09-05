# Arya Banking BOM

Bill of Materials — centralizes dependency versions for all Arya Banking services.

## Usage

```xml
<dependencyManagement>
    <dependencies>
        <dependency>
            <groupId>org.arya.banking</groupId>
            <artifactId>arya-banking-bom</artifactId>
            <version>2.0.0</version>
            <type>pom</type>
            <scope>import</scope>
        </dependency>
    </dependencies>
</dependencyManagement>
```

## What It Manages

Common modules (`core`, `mongo`, `kafka`, `feign`, `oauth2`, `outbox-service`), plus `lombok`, `mapstruct`, `gson`, `avro`, `confluent`, `spring-boot-dependencies`, and `spring-cloud-dependencies`.

## Build

```sh
mvn clean install
```

## Links

- [Docs](https://event-based-banking-application.github.io/arya-banking/docs/maven-registry/)
- [Common Library](https://github.com/Event-Based-Banking-Application/arya-banking-common)
