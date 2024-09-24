# K8SAPP: Harbor HA with PostgreSQL and Redis

This K8SAPP is a full HA Harbor installation. This installation follows one industry practices called K8SAPP for managing core enterprise applications.

## Updating

The `resources/values.yaml` file was originally generated with the following command:

```sh
helm show values bitnami/harbor > resources/values.yaml
```

These values should be compared to those of new charts when updating.
