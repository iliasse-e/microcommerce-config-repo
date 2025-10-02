# microcommerce-config-repo

Dossier de configuration de l'application microcommerce :

https://github.com/iliasse-e/microcommerce.git

## Structure de la configuration

```textplain
config-repo/
├── application.properties              # Propriétés communes à tous les services (ex: Discovery / Actuator si necessaire)
├── commande-service-dev.properties     # Propriétés spécifiques à commande-service en profil dev (ex: H2 database / Resilience4J / Open Feign)
├── paiement-service-dev.properties     # Propriétés spécifiques à paiement-service en profil dev
├── product-dev.properties              # Propriétés spécifiques à product-service en profil dev
```

## La configuration maven

Pour les microservices :

```properties
<dependency>
  <groupId>org.springframework.cloud</groupId>
  <artifactId>spring-cloud-starter-config</artifactId>
</dependency>
```

Pour le server de configuration :

```properties
<dependency>
  <groupId>org.springframework.cloud</groupId>
  <artifactId>spring-cloud-config-server</artifactId>
</dependency>
```
