# quarkus-azure-asb

This project uses Quarkus, the Supersonic Subatomic Java Framework.

If you want to learn more about Quarkus, please visit its website: <https://quarkus.io/>.

## Running the application in dev mode

You can run your application in dev mode that enables live coding using:

```shell script
./mvnw compile quarkus:dev
```

> **_NOTE:_**  Quarkus now ships with a Dev UI, which is available in dev mode only at <http://localhost:8080/q/dev/>.

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
./mvnw package -Dquarkus.package.jar.type=uber-jar
```

The application, packaged as an _über-jar_, is now runnable using `java -jar target/*-runner.jar`.

## Creating a native executable

You can create a native executable using:

```shell script
./mvnw package -Dnative
```

Or, if you don't have GraalVM installed, you can run the native executable build in a container using:

```shell script
./mvnw package -Dnative -Dquarkus.native.container-build=true
```

You can then execute your native executable with: `./target/quarkus-azure-asb-1.0.0-SNAPSHOT-runner`

If you want to learn more about building native executables, please consult <https://quarkus.io/guides/maven-tooling>.

## Related Guides

- Camel XQuery ([guide](https://camel.apache.org/camel-quarkus/latest/reference/extensions/saxon.html)): Query and/or transform XML payloads using XQuery and Saxon
- Camel Core ([guide](https://camel.apache.org/camel-quarkus/latest/reference/extensions/core.html)): Camel core functionality and basic Camel languages: Constant, ExchangeProperty, Header, Ref, Simple and Tokenize
- Camel Bindy ([guide](https://camel.apache.org/camel-quarkus/latest/reference/extensions/bindy.html)): Marshal and unmarshal between POJOs on one side and Comma separated values (CSV), fixed field length or key-value pair (KVP) formats on the other side using Camel Bindy
- Camel Quartz ([guide](https://camel.apache.org/camel-quarkus/latest/reference/extensions/quartz.html)): Schedule sending of messages using the Quartz 2.x scheduler
- Camel JPA ([guide](https://camel.apache.org/camel-quarkus/latest/reference/extensions/jpa.html)): Store and retrieve Java objects from databases using Java Persistence API (JPA)
- Camel Data Format ([guide](https://camel.apache.org/camel-quarkus/latest/reference/extensions/dataformat.html)): Use a Camel Data Format as a regular Camel Component
- Camel Azure Event Hubs ([guide](https://camel.apache.org/camel-quarkus/latest/reference/extensions/azure-eventhubs.html)): The azure-eventhubs component that integrates Azure Event Hubs using AMQP protocol. Azure EventHubs is a highly scalable publish-subscribe service that can ingest millions of events per second and stream them to multiple consumers
- Camel XPath ([guide](https://camel.apache.org/camel-quarkus/latest/reference/extensions/xpath.html)): Evaluates an XPath expression against an XML payload
- Camel AMQP ([guide](https://camel.apache.org/camel-quarkus/latest/reference/extensions/amqp.html)): Messaging with AMQP protocol using Apache QPid Client
- Camel Log ([guide](https://camel.apache.org/camel-quarkus/latest/reference/extensions/log.html)): Prints data form the routed message (such as body and headers) to the logger
- Camel CSV ([guide](https://camel.apache.org/camel-quarkus/latest/reference/extensions/csv.html)): Handle CSV (Comma Separated Values) payloads
- Camel Validator ([guide](https://camel.apache.org/camel-quarkus/latest/reference/extensions/validator.html)): Validate the payload using XML Schema and JAXP Validation
- Azure Functions HTTP ([guide](https://quarkus.io/guides/azure-functions-http)): Write Microsoft Azure functions
- OpenTelemetry ([guide](https://quarkus.io/guides/opentelemetry)): Use OpenTelemetry to trace services
- Camel JDBC ([guide](https://camel.apache.org/camel-quarkus/latest/reference/extensions/jdbc.html)): Access databases through SQL and JDBC
- Mutiny ([guide](https://quarkus.io/guides/mutiny-primer)): Write reactive applications with the modern Reactive Programming library Mutiny
- AMQP 1.0 JMS client - Apache Qpid JMS ([guide](https://quarkus.io/guides/jms)): Use JMS APIs with AMQP 1.0 servers such as ActiveMQ Artemis, ActiveMQ 5, Qpid Broker-J, Qpid Dispatch router, Azure Service Bus, and more
- Camel File ([guide](https://camel.apache.org/camel-quarkus/latest/reference/extensions/file.html)): Read and write files
- Camel XJ ([guide](https://camel.apache.org/camel-quarkus/latest/reference/extensions/xj.html)): Transform JSON and XML message using a XSLT
- Camel CXF ([guide](https://camel.apache.org/camel-quarkus/latest/reference/extensions/cxf-soap.html)): Expose SOAP WebServices using Apache CXF or connect to external WebServices using CXF WS client
- Quarkus CXF Metrics ([guide](https://quarkiverse.github.io/quarkiverse-docs/quarkus-cxf/dev/reference/extensions/quarkus-cxf-rt-features-metrics.html)): Collect metrics using https://micrometer.io/[Micrometer].
- Camel Base64 ([guide](https://camel.apache.org/camel-quarkus/latest/reference/extensions/base64.html)): Encode and decode data using Base64
- Camel MapStruct ([guide](https://camel.apache.org/camel-quarkus/latest/reference/extensions/mapstruct.html)): Type Conversion using Mapstruct
- Camel Direct ([guide](https://camel.apache.org/camel-quarkus/latest/reference/extensions/direct.html)): Call another endpoint from the same Camel Context synchronously
- Camel Jackson ([guide](https://camel.apache.org/camel-quarkus/latest/reference/extensions/jackson.html)): Marshal POJOs to JSON and back using Jackson
- Camel Caffeine Cache ([guide](https://camel.apache.org/camel-quarkus/latest/reference/extensions/caffeine.html)): Perform caching operations using Caffeine Cache
- Camel Bean ([guide](https://camel.apache.org/camel-quarkus/latest/reference/extensions/bean.html)): Invoke methods of Java beans
- Logging JSON ([guide](https://quarkus.io/guides/logging#json-logging)): Add JSON formatter for console logging
- SmallRye Metrics ([guide](https://quarkus.io/guides/smallrye-metrics)): Expose metrics for your services
- Camel Gson ([guide](https://camel.apache.org/camel-quarkus/latest/reference/extensions/gson.html)): Marshal POJOs to JSON and back using Gson
- Camel REST OpenApi ([guide](https://camel.apache.org/camel-quarkus/latest/reference/extensions/rest-openapi.html)): To call REST services using OpenAPI specification as contract
- Camel XSLT ([guide](https://camel.apache.org/camel-quarkus/latest/reference/extensions/xslt.html)): Transforms XML payload using an XSLT template
- Micrometer metrics ([guide](https://quarkus.io/guides/micrometer)): Instrument the runtime and your application with dimensional metrics using Micrometer.
- Camel OpenTelemetry ([guide](https://camel.apache.org/camel-quarkus/latest/reference/extensions/opentelemetry.html)): Distributed tracing using OpenTelemetry
- Camel OpenAPI Java ([guide](https://camel.apache.org/camel-quarkus/latest/reference/extensions/openapi-java.html)): Expose OpenAPI resources defined in Camel REST DSL
- Camel Azure Storage Queue Service ([guide](https://camel.apache.org/camel-quarkus/latest/reference/extensions/azure-storage-queue.html)): The azure-storage-queue component is used for storing and retrieving the messages to/from Azure Storage Queue using Azure SDK v12
- Camel JacksonXML ([guide](https://camel.apache.org/camel-quarkus/latest/reference/extensions/jacksonxml.html)): Unmarshal an XML payloads to POJOs and back using XMLMapper extension of Jackson
- Camel JSLT ([guide](https://camel.apache.org/camel-quarkus/latest/reference/extensions/jslt.html)): Query or transform JSON payloads using an JSLT
- Camel Bean Validator ([guide](https://camel.apache.org/camel-quarkus/latest/reference/extensions/bean-validator.html)): Validate the message body using the Java Bean Validation API
- Camel MicroProfile Health ([guide](https://camel.apache.org/camel-quarkus/latest/reference/extensions/microprofile-health.html)): Expose Camel health checks via MicroProfile Health
- CXF XJC Plugins ([guide](https://quarkiverse.github.io/quarkiverse-docs/quarkus-cxf/dev/reference/extensions/quarkus-cxf-xjc-plugins.html)): CXF XJC plugins for wsdl2java code generation
- Camel Micrometer ([guide](https://camel.apache.org/camel-quarkus/latest/reference/extensions/micrometer.html)): Collect various metrics directly from Camel routes using the Micrometer library
- Quarkus CXF OpenTelemetry ([guide](https://quarkiverse.github.io/quarkiverse-docs/quarkus-cxf/dev/reference/extensions/quarkus-cxf-integration-tracing-opentelemetry.html)): Collect metrics using https://micrometer.io/[Micrometer].
- Camel Rest ([guide](https://camel.apache.org/camel-quarkus/latest/reference/extensions/rest.html)): Expose REST services and their OpenAPI Specification or call external REST services

## Provided Code
