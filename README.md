# Service Registry for E-commerce Application

This project is a service registry for an e-commerce application using Eureka. The service registry plays a crucial role in a microservices architecture by enabling the discovery and communication between different services. By centralizing service registration and discovery, it simplifies the management of service instances and helps maintain the health and availability of the e-commerce platform.

## Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Prerequisites](#prerequisites)
- [Installation](#installation)
- [Configuration](#configuration)
- [Running the Service](#running-the-service)
- [Testing](#testing)
- [Contributing](#contributing)
- [License](#license)

## Overview

The Service Registry is built using [Spring Cloud Netflix Eureka](https://cloud.spring.io/spring-cloud-netflix/multi/multi__service_discovery_eureka_clients.html). It is a critical component in our microservices architecture, enabling service discovery and registration for the various components of the e-commerce platform.

### Key Responsibilities

- **Service Registration:** Each microservice registers itself with the Eureka server, providing metadata such as host, port, and health status.
- **Service Discovery:** Microservices query the Eureka server to find other registered services, allowing them to communicate with each other dynamically.
- **Health Monitoring:** Eureka server periodically checks the health of registered services to ensure they are available and functioning correctly.

## Features

- **Service Discovery:** Allows microservices to find and communicate with each other.
- **High Availability:** Configured to run in a cluster for high availability and resilience.
- **Self-preservation Mode:** Ensures the registry remains available even during network partitions.

## Prerequisites

- Java 17 or higher
- Maven 3.6.3 or higher
- Spring Boot 3 or higher

## Installation

1. Clone the repository:

    ```sh
    git clone https://github.com/Agustin199811/service-registry.git
    ```

2. Build the project using Maven:

    ```sh
    mvn clean install
    ```

## Configuration

The configuration for Eureka Server is located in `src/main/resources/application.properties`. Below is an example configuration:

```properties
server.port=8761

eureka.client.register-with-eureka=false
eureka.client.fetch-registry=false
eureka.server.wait-time-in-ms-when-sync-empty=0
```

## Running the Service

To run the service registry, use the following command:

 ```sh
    mvn spring-boot:run
```

## Testing

To test if the service registry is working correctly, you can register a sample microservice and verify its presence in the Eureka dashboard.

1. Run the service registry.
2. Start a sample microservice that includes Eureka Client configuration.
3. Check the Eureka dashboard to see the registered instances

## Contributing

Contributions are welcome! If you would like to contribute to this project, please send us an email at
`toapantaagustin9c@gmail.com` with details about your proposed changes or improvements. We look forward to hearing from you!

## License

This project is licensed under the MIT License - see the LICENSE file for details.
