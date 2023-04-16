# code-with-quarkus-maven

This project uses Quarkus, the Supersonic Subatomic Java Framework.

If you want to learn more about Quarkus, please visit its website: https://quarkus.io/ .

## Running the application in dev mode

You can run your application in dev mode that enables live coding using:
```shell script
./mvnw compile quarkus:dev
```

> **_NOTE:_**  Quarkus now ships with a Dev UI, which is available in dev mode only at http://localhost:8080/q/dev/.

## Packaging and running the application

The application can be packaged using:
```shell script
./mvnw package
```
It produces the `quarkus-run.jar` file in the `target/quarkus-app/` directory.
Be aware that it’s not an _über-jar_ as the dependencies are copied into the `target/quarkus-app/lib/` directory.

The application is now runnable using `java -jar target/quarkus-app/quarkus-run.jar`.

If you want to build an _über-jar_, execute the following command:
```shell script
./mvnw package -Dquarkus.package.type=uber-jar
```

The application, packaged as an _über-jar_, is now runnable using `java -jar target/*-runner.jar`.

## Creating a native executable

You can create a native executable using: 
```shell script
./mvnw package -Pnative
```

Or, if you don't have GraalVM installed, you can run the native executable build in a container using: 
```shell script
./mvnw package -Pnative -Dquarkus.native.container-build=true
```

You can then execute your native executable with: `./target/code-with-quarkus-maven-1.0.0-SNAPSHOT-runner`

If you want to learn more about building native executables, please consult https://quarkus.io/guides/maven-tooling.

## Related Guides

- Camel Slack ([guide](https://camel.apache.org/camel-quarkus/latest/reference/extensions/slack.html)): Send and receive messages to/from Slack
- OpenID Connect Client ([guide](https://quarkus.io/guides/security-openid-connect-client)): Get and refresh access tokens from OpenID Connect providers
- OpenID Connect Client Filter Reactive ([guide](https://quarkus.io/guides/security-openid-connect-client)): Use Reactive RestClient filter to get and refresh access tokens with OpenId Connect Client and send them as HTTP Authorization Bearer tokens
- Camel Quartz ([guide](https://camel.apache.org/camel-quarkus/latest/reference/extensions/quartz.html)): Schedule sending of messages using the Quartz 2.x scheduler
- SmallRye JWT ([guide](https://quarkus.io/guides/security-jwt)): Secure your applications with JSON Web Token
- Apache POI ([guide](https://quarkiverse.github.io/quarkiverse-docs/quarkus-poi/dev/)): Read and write files in Microsoft Office formats, such as Word, Excel and PowerPoint
- Dashbuilder ([guide](https://quarkiverse.github.io/quarkiverse-docs/quarkus-dashbuilder/dev/index.html)): Dashbuilder extension for embedding dashboards in a Quarkus application
- OpenTelemetry ([guide](https://quarkus.io/guides/opentelemetry)): Use OpenTelemetry to trace services
- Camel JDBC ([guide](https://camel.apache.org/camel-quarkus/latest/reference/extensions/jdbc.html)): Access databases through SQL and JDBC
- Minikube ([guide](https://quarkus.io/guides/kubernetes)): Generate Minikube resources from annotations
- REST Client Classic ([guide](https://quarkus.io/guides/rest-client)): Call REST services
- Apache Avro ([guide](https://quarkus.io/guides/kafka)): Provide support for the Avro data serialization system
- Camel iCal ([guide](https://camel.apache.org/camel-quarkus/latest/reference/extensions/ical.html)): Marshal and unmarshal iCal (.ics) documents to/from model objects
- REST resources for Hibernate Reactive with Panache ([guide](https://quarkus.io/guides/rest-data-panache)): Generate Jakarta REST resources for your Hibernate Reactive Panache entities and repositories
- Camel Gson ([guide](https://camel.apache.org/camel-quarkus/latest/reference/extensions/gson.html)): Marshal POJOs to JSON and back using Gson
- Kubernetes ([guide](https://quarkus.io/guides/kubernetes)): Generate Kubernetes resources from annotations
- Camel Kafka ([guide](https://camel.apache.org/camel-quarkus/latest/reference/extensions/kafka.html)): Sent and receive messages to/from an Apache Kafka broker
- Camel Bean Validator ([guide](https://camel.apache.org/camel-quarkus/latest/reference/extensions/bean-validator.html)): Validate the message body using the Java Bean Validation API
- Camel MicroProfile Health ([guide](https://camel.apache.org/camel-quarkus/latest/reference/extensions/microprofile-health.html)): Expose Camel health checks via MicroProfile Health
- Narayana STM - Software Transactional Memory ([guide](https://quarkus.io/guides/software-transactional-memory)): Offer Software Transactional Memory (stm) support
- Liquibase ([guide](https://quarkus.io/guides/liquibase)): Handle your database schema migrations with Liquibase
- Camel Micrometer ([guide](https://camel.apache.org/camel-quarkus/latest/reference/extensions/micrometer.html)): Collect various metrics directly from Camel routes using the Micrometer library
- Kubernetes Config ([guide](https://quarkus.io/guides/kubernetes-config)): Read runtime configuration from Kubernetes ConfigMaps and Secrets
- Cache ([guide](https://quarkus.io/guides/cache)): Enable application data caching in CDI beans
- Camel PDF ([guide](https://camel.apache.org/camel-quarkus/latest/reference/extensions/pdf.html)): Create, modify or extract content from PDF documents
- Camel gRPC ([guide](https://camel.apache.org/camel-quarkus/latest/reference/extensions/grpc.html)): Expose gRPC endpoints and access external gRPC endpoints
- Logging Sentry ([guide](https://quarkiverse.github.io/quarkiverse-docs/quarkus-logging-sentry/dev/index.html)): Use Sentry, a self-hosted or cloud-based error monitoring solution
- Camel Minio ([guide](https://camel.apache.org/camel-quarkus/latest/reference/extensions/minio.html)): Store and retrieve objects from Minio Storage Service using Minio SDK
- SmallRye Fault Tolerance ([guide](https://quarkus.io/guides/smallrye-fault-tolerance)): Build fault-tolerant network services
- Scheduler ([guide](https://quarkus.io/guides/scheduler)): Schedule jobs and tasks
- Camel Debezium PostgresSQL Connector ([guide](https://camel.apache.org/camel-quarkus/latest/reference/extensions/debezium-postgres.html)): Capture changes from a PostgresSQL database
- SmallRye Stork ([guide](https://quarkus.io/guides/stork)): Support for SmallRye Stork
- Camel CSV ([guide](https://camel.apache.org/camel-quarkus/latest/reference/extensions/csv.html)): Handle CSV (Comma Separated Values) payloads
- Camel Avro Jackson ([guide](https://camel.apache.org/camel-quarkus/latest/reference/extensions/jackson-avro.html)): Marshal POJOs to Avro and back using Jackson
- Camel File Watch ([guide](https://camel.apache.org/camel-quarkus/latest/reference/extensions/file-watch.html)): Get notified about file events in a directory using java.nio.file.WatchService
- Hibernate ORM with Panache ([guide](https://quarkus.io/guides/hibernate-orm-panache)): Simplify your persistence code for Hibernate ORM via the active record or the repository pattern
- OpenID Connect Token Propagation ([guide](https://quarkus.io/guides/security-openid-connect-client)): Use Jakarta REST Client filter to propagate the incoming Bearer access token or token acquired from Authorization Code Flow as HTTP Authorization Bearer token
- Camel Knative ([guide](https://camel.apache.org/camel-quarkus/latest/reference/extensions/knative.html)): Send and receive events from Knative
- Reactive Routes ([guide](https://quarkus.io/guides/reactive-routes)): REST framework offering the route model to define non blocking endpoints
- REST Client Reactive ([guide](https://quarkus.io/guides/rest-client-reactive)): Call REST services reactively
- Camel Consul ([guide](https://camel.apache.org/camel-quarkus/latest/reference/extensions/consul.html)): Integrate with Consul service discovery and configuration store
- RESTEasy Reactive ([guide](https://quarkus.io/guides/resteasy-reactive)): A Jakarta REST implementation utilizing build time processing and Vert.x. This extension is not compatible with the quarkus-resteasy extension, or any of the extensions that depend on it.
- OpenID Connect Client Filter ([guide](https://quarkus.io/guides/security-openid-connect-client)): Use Jakarta REST Client filter to get and refresh access tokens with OpenId Connect Client and send them as HTTP Authorization Bearer tokens
- Camel Avro ([guide](https://camel.apache.org/camel-quarkus/latest/reference/extensions/avro.html)): Serialize and deserialize messages using Apache Avro binary data format
- Camel Caffeine Cache ([guide](https://camel.apache.org/camel-quarkus/latest/reference/extensions/caffeine.html)): Perform caching operations using Caffeine Cache
- Logging JSON ([guide](https://quarkus.io/guides/logging#json-logging)): Add JSON formatter for console logging
- OpenID Connect Token Propagation Reactive ([guide](https://quarkus.io/guides/security-openid-connect-client)): Use Reactive REST Client to propagate the incoming Bearer access token or token acquired from Authorization Code Flow as HTTP Authorization Bearer token
- REST resources for Hibernate ORM with Panache ([guide](https://quarkus.io/guides/rest-data-panache)): Generate Jakarta REST resources for your Hibernate Panache entities and repositories
- Elasticsearch Java Client ([guide](https://quarkus.io/guides/elasticsearch)): Connect to an Elasticsearch cluster using the Java client
- Micrometer Registry Prometheus ([guide](https://quarkus.io/guides/micrometer)): Enable Prometheus support for Micrometer
- Hibernate Validator ([guide](https://quarkus.io/guides/validation)): Validate object properties (field, getter) and method parameters for your beans (REST, CDI, Jakarta Persistence)
- Logging GELF ([guide](https://quarkus.io/guides/centralized-log-management)): Log using the Graylog Extended Log Format and centralize your logs in ELK or EFK
- Camel Kubernetes ([guide](https://camel.apache.org/camel-quarkus/latest/reference/extensions/kubernetes.html)): Perform operations against Kubernetes API
- Camel JTA ([guide](https://camel.apache.org/camel-quarkus/latest/reference/extensions/jta.html)): Enclose Camel routes in transactions using Java Transaction API (JTA) and Narayana transaction manager
- Qute ([guide](https://quarkus.io/guides/qute)): Offer templating support for web, email, etc in a build time, type-safe way
- Kind ([guide](https://quarkus.io/guides/kubernetes)): Generate Kind resources from annotations
- Elasticsearch REST client ([guide](https://quarkus.io/guides/elasticsearch)): Connect to an Elasticsearch cluster using the REST low level client
- Camel Microprofile Fault Tolerance ([guide](https://camel.apache.org/camel-quarkus/latest/reference/extensions/microprofile-fault-tolerance.html)): Circuit Breaker EIP using Microprofile Fault Tolerance
- JDBC Driver - PostgreSQL ([guide](https://quarkus.io/guides/datasource)): Connect to the PostgreSQL database via JDBC
- Keycloak Authorization ([guide](https://quarkus.io/guides/security-keycloak-authorization)): Policy enforcer using Keycloak-managed permissions to control access to protected resources
- Confluent Schema Registry - Avro ([guide](https://quarkus.io/guides/kafka-schema-registry-avro)): Use Confluent as Avro schema registry
- Kubernetes Client ([guide](https://quarkus.io/guides/kubernetes-client)): Interact with Kubernetes and develop Kubernetes Operators
- Jacoco - Code Coverage ([guide](https://quarkus.io/guides/tests-with-coverage)): Jacoco test coverage support
- Mailer ([guide](https://quarkus.io/guides/mailer)): Send emails
- Camel Jackson ([guide](https://camel.apache.org/camel-quarkus/latest/reference/extensions/jackson.html)): Marshal POJOs to JSON and back using Jackson
- Vault ([guide](https://quarkiverse.github.io/quarkiverse-docs/quarkus-vault/dev/index.html)): Store your credentials securely in HashiCorp Vault
- Camel JSON Schema Validator ([guide](https://camel.apache.org/camel-quarkus/latest/reference/extensions/json-validator.html)): Validate JSON payloads using NetworkNT JSON Schema
- SmallRye Context Propagation ([guide](https://quarkus.io/guides/context-propagation)): Propagate contexts between managed threads in reactive applications
- Camel OpenTelemetry ([guide](https://camel.apache.org/camel-quarkus/latest/reference/extensions/opentelemetry.html)): Distributed tracing using OpenTelemetry
- Camel Reactive Executor ([guide](https://camel.apache.org/camel-quarkus/latest/reference/extensions/reactive-executor.html)): Reactive Executor for camel-core using Vert.x
- SmallRye Reactive Messaging ([guide](https://quarkus.io/guides/reactive-messaging)): Produce and consume messages and implement event driven and data streaming applications
- Quartz ([guide](https://quarkus.io/guides/quartz)): Schedule clustered tasks with Quartz
- Redis Cache ([guide](https://quarkus.io/guides/cache-redis-reference)): Use Redis as the caching backend
- Redis Client ([guide](https://quarkus.io/guides/redis)): Connect to Redis in either imperative or reactive style
- Camel Zip File ([guide](https://camel.apache.org/camel-quarkus/latest/reference/extensions/zipfile.html)): Compression and decompress streams using java.util.zip.ZipStream
- SmallRye JWT Build ([guide](https://quarkus.io/guides/security-jwt-build)): Create JSON Web Token with SmallRye JWT Build API
- Camel LRA ([guide](https://camel.apache.org/camel-quarkus/latest/reference/extensions/lra.html)): Camel saga binding for Long-Running-Action framework
- Narayana LRA - LRA Participant Support ([guide](https://quarkus.io/guides/lra)): Coordinate Long Running Actions (LRA)
- Camel Debezium SQL Server Connector ([guide](https://camel.apache.org/camel-quarkus/latest/reference/extensions/debezium-sqlserver.html)): Capture changes from an SQL Server database
- Camel JSON Path ([guide](https://camel.apache.org/camel-quarkus/latest/reference/extensions/jsonpath.html)): Evaluate a JSONPath expression against a JSON message body
- Camel Jira ([guide](https://camel.apache.org/camel-quarkus/latest/reference/extensions/jira.html)): Interact with JIRA issue tracker
- SmallRye OpenAPI ([guide](https://quarkus.io/guides/openapi-swaggerui)): Document your REST APIs with OpenAPI - comes with Swagger UI
- Picocli ([guide](https://quarkus.io/guides/picocli)): Develop command line applications with Picocli
- SmallRye Reactive Messaging - Kafka Connector ([guide](https://quarkus.io/guides/kafka-reactive-getting-started)): Connect to Kafka with Reactive Messaging
- Apache Kafka Streams ([guide](https://quarkus.io/guides/kafka-streams)): Implement stream processing applications based on Apache Kafka
- Camel Mail ([guide](https://camel.apache.org/camel-quarkus/latest/reference/extensions/mail.html)): Send and receive emails using imap, pop3 and smtp protocols
- Camel Reactive Streams ([guide](https://camel.apache.org/camel-quarkus/latest/reference/extensions/reactive-streams.html)): Exchange messages with reactive stream processing libraries compatible with the reactive streams standard
- Camel Cassandra CQL ([guide](https://camel.apache.org/camel-quarkus/latest/reference/extensions/cassandraql.html)): Integrate with Cassandra 2.0 using the CQL3 API (not the Thrift API). Based on Cassandra Java Driver provided by DataStax
- Camel File ([guide](https://camel.apache.org/camel-quarkus/latest/reference/extensions/file.html)): Read and write files
- RESTEasy Reactive Links ([guide](https://quarkus.io/guides/resteasy-reactive#web-links-support)): Web Links support for RESTEasy Reactive. Inject web links into response HTTP headers by annotating your endpoint resources.
- Apache Kafka Client ([guide](https://quarkus.io/guides/kafka)): Connect to Apache Kafka with its native API
- Consul Config ([guide](https://quarkiverse.github.io/quarkiverse-docs/quarkus-config-extensions/dev/consul.html)): Read runtime configuration from Consul Key - Value store
- Apache Tika ([guide](https://quarkiverse.github.io/quarkiverse-docs/quarkus-tika/dev/index.html)): Extract data from your documents with Apache Tika
- Camel Bean ([guide](https://camel.apache.org/camel-quarkus/latest/reference/extensions/bean.html)): Invoke methods of Java beans
- SmallRye Health ([guide](https://quarkus.io/guides/microprofile-health)): Monitor service health
- RESTEasy Classic Links ([guide](https://quarkus.io/guides/resteasy#links)): Web Links support for RESTEasy Classic. Inject web links into response HTTP headers by annotating your endpoint resources.
- Micrometer metrics ([guide](https://quarkus.io/guides/micrometer)): Instrument the runtime and your application with dimensional metrics using Micrometer.
- Camel Exec ([guide](https://camel.apache.org/camel-quarkus/latest/reference/extensions/exec.html)): Execute commands on the underlying operating system
- Camel JSLT ([guide](https://camel.apache.org/camel-quarkus/latest/reference/extensions/jslt.html)): Query or transform JSON payloads using an JSLT
- OpenID Connect ([guide](https://quarkus.io/guides/security-openid-connect)): Verify Bearer access tokens and authenticate users with Authorization Code Flow
- Camel Protobuf ([guide](https://camel.apache.org/camel-quarkus/latest/reference/extensions/protobuf.html)): Serialize and deserialize Java objects using Google's Protocol buffers
- Camel Zip Deflate Compression ([guide](https://camel.apache.org/camel-quarkus/latest/reference/extensions/zip-deflater.html)): Compress and decompress streams using java.util.zip.Deflater, java.util.zip.Inflater or java.util.zip.GZIPStream
- Security JPA ([guide](https://quarkus.io/guides/security-getting-started)): Secure your applications with username/password stored in a database via Jakarta Persistence
- iText ([guide](https://quarkiverse.github.io/quarkiverse-docs/quarkus-itext/dev/)): Create and manipulate PDFs on the fly

## Provided Code

### gRPC

Create your first gRPC service

[Related guide section...](https://quarkus.io/guides/grpc-getting-started)

### Hibernate ORM

Create your first JPA entity

[Related guide section...](https://quarkus.io/guides/hibernate-orm)

[Related Hibernate with Panache section...](https://quarkus.io/guides/hibernate-orm-panache)


### Picocli Example

Hello and goodbye are civilization fundamentals. Let's not forget it with this example picocli application by changing the <code>command</code> and <code>parameters</code>.

[Related guide section...](https://quarkus.io/guides/picocli#command-line-application-with-multiple-commands)

Also for picocli applications the dev mode is supported. When running dev mode, the picocli application is executed and on press of the Enter key, is restarted.

As picocli applications will often require arguments to be passed on the commandline, this is also possible in dev mode via:
```shell script
./mvnw compile quarkus:dev -Dquarkus.args='Quarky'
```

### Reactive Messaging codestart

Use SmallRye Reactive Messaging

[Related Apache Kafka guide section...](https://quarkus.io/guides/kafka-reactive-getting-started)


### REST Client

Invoke different services through REST with JSON

[Related guide section...](https://quarkus.io/guides/rest-client)

### RESTEasy JAX-RS

Easily start your RESTful Web Services

[Related guide section...](https://quarkus.io/guides/getting-started#the-jax-rs-resources)

### RESTEasy Reactive

Easily start your Reactive RESTful Web Services

[Related guide section...](https://quarkus.io/guides/getting-started-reactive#reactive-jax-rs-resources)

### SmallRye Health

Monitor your application's health using SmallRye Health

[Related guide section...](https://quarkus.io/guides/smallrye-health)
