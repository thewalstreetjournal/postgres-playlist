You can build the container using:

```bash
docker build -t postgres-17.6:v1 .
docker network create pgnet
docker run -d --name postgres --network pgnet -e POSTGRES_PASSWORD=secret po    stgres-17.6:v1 && docker exec -it postgres bash
```
