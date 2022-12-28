postgres:
    docker run --name postgres15 -p 5432:5432 -e POSTGRES_USER=root -e POSTGRES_PASSWORD=secret -d postgres:15-alpine

createdb:
    docker exec -it postgres15 createdb --username=root --owner=root simple_bank

dropdb:
    docker exec -it postgres15 dropdb simple_bank

sqlc:
	sqlc generate

.PHONY: postgres createdb dropdb sqlc