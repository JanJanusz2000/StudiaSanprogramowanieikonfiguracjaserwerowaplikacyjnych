# programowanieikonfiguracjaserwerowaplikacyjnych

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
./mvnw package -Dnative
```

Or, if you don't have GraalVM installed, you can run the native executable build in a container using:

```shell script
./mvnw package -Dnative -Dquarkus.native.container-build=true
```

You can then execute your native executable
with: `./target/programowanieikonfiguracjaserwerowaplikacyjnych-1.0-SNAPSHOT-runner`

If you want to learn more about building native executables, please consult https://quarkus.io/guides/maven-tooling.

## Related Guides

- Camel XJ ([guide](https://camel.apache.org/camel-quarkus/latest/reference/extensions/xj.html)): Transform JSON and XML
  message using a XSLT
- RESTEasy Classic JSON-B ([guide](https://quarkus.io/guides/rest-json)): JSON-B serialization support for RESTEasy
  Classic
- Camel Jackson ([guide](https://camel.apache.org/camel-quarkus/latest/reference/extensions/jackson.html)): Marshal
  POJOs to JSON and back using Jackson
- Logging JSON ([guide](https://quarkus.io/guides/logging#json-logging)): Add JSON formatter for console logging
- Camel JSON Schema
  Validator ([guide](https://camel.apache.org/camel-quarkus/latest/reference/extensions/json-validator.html)): Validate
  JSON payloads using NetworkNT JSON Schema
- Camel Gson ([guide](https://camel.apache.org/camel-quarkus/latest/reference/extensions/gson.html)): Marshal POJOs to
  JSON and back using Gson
- Camel JSON Path ([guide](https://camel.apache.org/camel-quarkus/latest/reference/extensions/jsonpath.html)): Evaluate
  a JSONPath expression against a JSON message body
- RESTEasy Classic's REST Client JSON-B ([guide](https://quarkus.io/guides/resteasy-client)): JSON-B serialization
  support for the REST client
- Camel JOLT ([guide](https://camel.apache.org/camel-quarkus/latest/reference/extensions/jolt.html)): JSON to JSON
  transformation using JOLT
- Hibernate Validator ([guide](https://quarkus.io/guides/validation)): Validate object properties (field, getter) and
  method parameters for your beans (REST, CDI, Jakarta Persistence)
- Camel JSLT ([guide](https://camel.apache.org/camel-quarkus/latest/reference/extensions/jslt.html)): Query or transform
  JSON payloads using an JSLT
- Camel JQ ([guide](https://camel.apache.org/camel-quarkus/latest/reference/extensions/jq.html)): Evaluates a JQ
  expression against a JSON message body
- Cache ([guide](https://quarkus.io/guides/cache)): Enable application data caching in CDI beans

## Provided Code

### RESTEasy JAX-RS

Easily start your RESTful Web Services

[Related guide section...](https://quarkus.io/guides/getting-started#the-jax-rs-resources)

### RESTEasy Reactive

Easily start your Reactive RESTful Web Services

[Related guide section...](https://quarkus.io/guides/getting-started-reactive#reactive-jax-rs-resources)
