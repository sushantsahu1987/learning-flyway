### Flyway

        1. docker run --rm -v "$(pwd)/migrations:/flyway/sql" flyway/flyway -url=jdbc:h2:mem:test -user=sa migrate
        2. docker run --rm -v "$(pwd)/migrations:/flyway/sql" -v "$(pwd)/conf:/flyway/conf" flyway/flyway migrate
        3. docker run --rm -v "$(pwd)/migrations:/flyway/sql" -v "$(pwd)/conf2:/flyway/conf" --network=host flyway/flyway migrate

### Postgres

        1. docker run --name test-postgres -e POSTGRES_USER=test -e POSTGRES_PASSWORD=test123 -p 5432:5432 -d postgres
