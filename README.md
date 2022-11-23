```text
# copy docker-compose.yml
```

```shell
curl -LO https://raw.githubusercontent.com/bitnami/containers/main/bitnami/spark/docker-compose.yml
```

```text
# add volume

    volumes:
      - .:/opt/spark/
```

```shell
docker-compose up -d --build
```

```shell

docker exec -it <container_id> bash
```

```shell

val df = spark.read.format("csv").option("header", "true").load("/opt/spark/titanic.csv")

```

```shell
df.printSchema
```

```shell
df.select("Name", "Age").show()

```

```shell

df.select("Name", "Age").filter("Age > 30").show()
```


