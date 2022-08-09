# how-to-install-dynamo-db-in-local
how to install dynamo db in local

```
curl -O https://s3-us-west-2.amazonaws.com/dynamodb-local/dynamodb_local_latest.zip
unzip dynamodb_local_latest.zip
rm dynamodb_local_latest.zip
```

```
vi start_dynamo.sh
```

```
java -Djava.library.path=./DynamoDBLocal_lib -jar DynamoDBLocal.jar -sharedDb
```

```
bash start_dynamo.sh
```

test dynamo aws
```
vi ~/.bashrc
export LOCAL_DB='--endpoint-url http://localhost:8000'
source ~/.bashrc
```

```
aws dynamodb list-tables $LOCAL_DB
```
