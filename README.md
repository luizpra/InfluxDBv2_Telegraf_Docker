# InfluxDBv2_Telegraf_Docker
Run InfluxDB 2.0 and Telegraf in containers

To learn more please read this blog on [Running InfluxDB 2.0 and Telegraf Using Docker](https://www.influxdata.com/blog/running-influxdb-2-0-and-telegraf-using-docker/)

## Running with docker compose

The `docker-compose.yaml` file rely on `influxdb2.env` variables to run, so use this command to run the stack.
```
docker-compose  --env-file influxv2.env  up
```

# Telegraf 

## Configuration

The `telegraf` app need a [config file](./telegraf/mytelegraf.conf) mapped to `/etc/telegraf/telegraf.conf`. This file should have `inputs` and `outputs` definitions. The following file will show how this file should be.

```conf
[agent]
...
[[outputs.influxdb_v2]]
...
[[inputs.cpu]]
```

Refer to [influx docs](https://docs.influxdata.com/influxdb/v2.4/write-data/no-code/use-telegraf/manual-config/) to see how use/conifgure telegraf.



# References

* [DockerHub Influxdb](https://hub.docker.com/_/influxdb)
* [Telegraf Configuration](https://www.influxdata.com/blog/telegraf-configuration-in-influxdb-2-0/)
* [Telegraf manual config](https://docs.influxdata.com/influxdb/v2.4/write-data/no-code/use-telegraf/manual-config/)