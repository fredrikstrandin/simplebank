docker run --rm -v $(pwd):/src -w /src kjconroy/sqlc generate

go get github.com/lib/pq

https://github.com/golang-migrate/migrate/tree/master/cmd/migrate

migrate -path db/migration -database "postgres:/root:secret@localhost:5432/simple_bank?sslmode=disable" -verbose up

aws ecr create-repository --repository-name simplebank --region eu-west-2
{
    "repository": {
        "repositoryArn": "arn:aws:ecr:eu-west-2:161399655491:repository/simplebank",
        "registryId": "161399655491",
        "repositoryName": "simplebank",
        "repositoryUri": "161399655491.dkr.ecr.eu-west-2.amazonaws.com/simplebank",
        "createdAt": "2022-12-28T13:42:10+00:00",
        "imageTagMutability": "MUTABLE",
        "imageScanningConfiguration": {
            "scanOnPush": false
        },
        "encryptionConfiguration": {
            "encryptionType": "AES256"
        }
    }
}