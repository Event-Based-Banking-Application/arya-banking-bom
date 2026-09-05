# Arya Banking BOM

Bill of Materials for the Arya Banking microservices ecosystem. Centralizes dependency versions so consuming services declare no versions.

## What It Manages

### Common Modules

| Artifact | Description |
|---|---|
| `org.arya.banking:core` | Domain models, exceptions, DTOs |
| `org.arya.banking:mongo` | MongoDB configuration |
| `org.arya.banking:kafka` | Kafka/Avro support |
| `org.arya.banking:feign` | Feign client config |
| `org.arya.banking:oauth2` | OAuth2 client credentials |
| `org.arya.banking:arya-banking-outbox-service` | Outbox pattern library |

### Third-Party Dependencies

- Lombok
- MapStruct + MapStruct Processor
- Gson
- Apache Avro
- Confluent Kafka Avro Serializer + Schema Registry Client
- Commons IO
- `spring-boot-dependencies` (BOM import)
- `spring-cloud-dependencies` (BOM import)

## Quick Start

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

<dependencies>
    <!-- No versions needed for managed artifacts -->
    <dependency>
        <groupId>org.arya.banking</groupId>
        <artifactId>core</artifactId>
    </dependency>
    <dependency>
        <groupId>org.projectlombok</groupId>
        <artifactId>lombok</artifactId>
    </dependency>
</dependencies>
```

## Build

```sh
mvn clean install          # install locally
mvn clean deploy -s settings.xml  # publish to GitHub Packages
```

## Links

- [Documentation](https://event-based-banking-application.github.io/arya-banking/docs/maven-registry/)
- [GitHub Packages](https://github.com/Event-Based-Banking-Application/arya-banking-bom/packages)
- [Common Library](https://github.com/Event-Based-Banking-Application/arya-banking-common)

## Maintainers

- [Karthik Kulkarni](https://github.com/karthikkulkarni)
