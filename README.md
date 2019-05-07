# GUI for DynamoDB Local 

## How to install

```
docker pull evheniy/docker-dynamodb-admin
```

## How to use

### Run

#### DynamoDB Local
```
docker run -d --name dynamodb -p 8000:8000 amazon/dynamodb-local
```

#### DynamoDB Admin Local
```
docker run -d --name dynamodb-admin -p 8001:8001 evheniy/docker-dynamodb-admin
```
Or with parameters:
```
docker run -d --name dynamodb-admin -p 3011:3011 -e DYNAMO_ENDPOINT=http://localhost:3010 -e PORT=3011 evheniy/docker-dynamodb-admin
```

## Stop

#### DynamoDB Local
```
docker rm -f dynamodb
```

#### DynamoDB Admin Local
```
docker rm -f dynamodb-admin
```

## Clean

#### DynamoDB Local
```
docker rmi -f amazon/dynamodb-local
```

#### DynamoDB Admin Local
```
docker rmi -f evheniy/docker-dynamodb-admin
```

# Clean all
```
docker system prune -a --volumes
```
