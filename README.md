# InfluxDBv2_Telegraf_Docker
Run InfluxDB 2.0 and Telegraf in containers

To learn more please read this blog on [Running InfluxDB 2.0 and Telegraf Using Docker](https://www.influxdata.com/blog/running-influxdb-2-0-and-telegraf-using-docker/)

## Running with docker compose

The `docker-compose.yaml` file rely on `influxdb2.env` variables to run, so use this command to run the stack.
```
docker-compose  --env-file influxv2.env  up
```

# References

* [DockerHub Influxdb](https://hub.docker.com/_/influxdb)