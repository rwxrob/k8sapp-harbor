# K8SAPP: Harbor HA with PostgreSQL and Redis

This K8SAPP is a full HA Harbor installation. This installation follows one industry practices called K8SAPP for managing core enterprise applications.

## Updating

The `resources/values*.yaml` files were originally generated with the following commands (before customization):

```sh
helm show values bitnami/postgresql --version 15.5.29 > resources/values-postgresql.yaml
helm show values bitnami/redis --version 20.1.0 > resources/values-redis.yaml
helm show values bitnami/harbor --version 23.0.3 > resources/values.yaml
```

The specific versions of the `postgresql` and `redis` charts were derived from the `Charts.lock` file.

Note that the `harbor` chart specifically overrides values from both the `postgresql` and `redis` charts (incorrectly in the case of `.postgresql.image.tag`).

These values should be compared to those of new charts when updating.
