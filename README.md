# Prebid Server (Java)

Prebid Server is an open source implementation of Server-Side Header Bidding.
It is managed by Prebid.org,
and upholds the principles from the [Prebid Code of Conduct](https://prebid.org/wrapper_code_of_conduct.html).

This project does not support the same set of Bidders as Prebid.js, although there is overlap.
The current set can be found in the [adapters](./src/main/java/org/prebid/server/bidder) package. If you don't see the one you want, feel free to [contribute it](docs/developers/add-new-bidder.md).

For more information, see:

# Getting Started

The server makes the following assumptions:
- No ranking or decisioning is performed by this server. It just proxies requests.
- No ad quality management (e.g., malware, viruses, deceptive creatives) is performed by this server.
- This server does no fraud scanning and does nothing to prevent bad traffic.
- This server logs errors but not requests.
- This server has no user profiling or user data collection capabilities.

This project is built upon [Vert.x](http://vertx.io) to achieve high request throughput. 
We use [Maven](https://maven.apache.org) and attempt to introduce minimal dependencies.

When running, the server responds to several HTTP [endpoints](docs/endpoints).

## Building

Follow next steps to create JAR file which can be deployed locally.

- Download or clone a project:

- Move to project directory:
```bash
cd prebid-server-java
```

- Run below command to build project:
```bash
mvn clean package
```

For more information how to configure the server follow [documentation](docs/build.md).

## Configuration

The source code includes minimal required configuration file `sample/prebid-config.yaml`.
Also, check the account settings file `sample/sample-app-settings.yaml`.

For more information how to configure the server follow [documentation](docs/config.md).


## Running

Run your local server with the command:
```bash
java -jar target/prebid-server.jar --spring.config.additional-location=sample/prebid-config.yaml
```

For more options how to start the server, please follow [documentation](docs/run.md).

## Verifying

To check the server is started go to [http://localhost:8080/status](http://localhost:8080/status) 
and verify response status is `200 OK`.

# Documentation

## Development
- [Endpoints](docs/endpoints)
- [Adding new bidder](docs/developers/add-new-bidder.md)
- [Adding new analytics module](docs/developers/add-new-analytics-module.md)
- [Adding viewability support](docs/developers/add-viewability-vendors.md)
- [Auction result post-processing](docs/developers/auction-result-post-processing.md)
- [Cookie Syncs](docs/developers/cookie-syncs.md)
- [Stored Requests](docs/developers/stored-requests.md)
- [Unit Tests](docs/developers/unit-tests.md)
- [GDPR](docs/developers/gdpr.md)

## Maintenance
- [Build for local](docs/build.md)
- [Build for AWS](docs/build-aws.md)
- [Configure application](docs/config.md)
  - [Full list of configuration options](docs/config-app.md)
  - [Application settings](docs/application-settings.md)
- [Run with optimizations](docs/run.md)
- [Metrics](docs/metrics.md)

## Contributing
- [Contributing](docs/contributing.md)
- [Code Style](docs/code-style.md)
- [Code Review](docs/code-reviews.md)
- [Versioning](docs/versioning.md)
