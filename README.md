docker run --rm -v $(pwd):/src -w /src kjconroy/sqlc generate

go get github.com/lib/pq

https://github.com/golang-migrate/migrate/tree/master/cmd/migrate

migrate -path db/migration -database "postgres:/root:secret@localhost:5432/simple_bank?sslmode=disable" -verbose up