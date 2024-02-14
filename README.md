# Simple Spring Boot RESTful Web Service

This project is a simple Spring Boot application that implements a RESTful web service. The web service provides a greeting message with a unique identifier, and it can be customized with a name parameter.

## GreetingController
The `GreetingController` class is the main controller responsible for handling HTTP requests. Here's a brief overview:

- **Endpoint**: The web service exposes a single endpoint /greeting.
- **Controller Method**:
    - The `greeting` method is annotated with @GetMapping("/greeting") to handle GET requests to the /greeting endpoint.
    - It takes an optional name parameter (default value is "World").
    - The method returns a Greeting object, which includes a unique ID generated using AtomicLong and a formatted greeting message.
AtomicLong:
- The AtomicLong instance (counter) ensures that the counter is updated atomically, making it suitable for concurrent access by multiple threads.

## Greeting Class

The `Greeting` class is a record class, and it automatically generates an immutable class with a constructor and accessor methods.

## Usage

To run the application, ensure you have Gradle installed. Then, run the following command in the project directory:
```bash
./gradlew bootRun
```

The application will start, and you can access the web service at http://localhost:8080/greeting. You can also customize the greeting message by providing a name parameter:
