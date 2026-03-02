# GuitarShop

A polyglot microservices e-commerce app for buying guitars and accessories.

## Services

| Service  | Language        | Data store | Description |
|----------|-----------------|------------|-------------|
| ui       | Java/Spring Boot| —          | Thymeleaf frontend |
| catalog  | Go              | MySQL      | Products and categories |
| cart     | Java/Spring Boot| Redis      | Per-customer shopping cart |
| checkout | Node.js         | PostgreSQL | Checkout sessions; publishes events to RabbitMQ |
| orders   | Java/Spring Boot| PostgreSQL | Order records; consumes events from RabbitMQ |

## Run

```bash
docker compose up
```

Then open [http://localhost:8080](http://localhost:8080).
