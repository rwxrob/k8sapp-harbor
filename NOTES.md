# Notes

* `build` script to build from primary sources on Internet
* `deploy` script to deploy fully into k8s cluster
* `undeploy` completely tear down the installation from the cluster
* `tools` directory for scripts called by others
* `tools/build-postgresql` called form `build`
* `tools/deploy-postgresql` called form `deploy`
* `tools/undeploy-postgresql` called form `undeploy`
* `tools/build-reddis` called form `build`
* `tools/deploy-reddis` called form `deploy`
* `tools/undeploy-reddis` called form `undeploy`
* automatic flattening of Helm chart into `kustomize` manifests
* remove all the stupid Helm shit form the manifests
* remove all secrets from manifests and replace with Vault fetch
* support for three main clusters: `prod`, `dev`, `inf`
* blue/green deployment model into any target cluster
* only bash scripting with `shellcheck` and `shfmt` linting
* support for web proxies in internal network scenarios
* install PostgreSQL, Reddis just for Harbor even though separate
* make PostgreSQL installation optional
* detect PostgreSQL installation and don't override unless explicit
* if undetected automatically install PostgreSQL
* include full backup of PostgreSQL k8s CronJobs
* single `harbor` namespace to keep ConfigMaps simple
* verify and validate external Vault installation dependency
* no attempt to `grep -va helm` out the helm stuff since does not work

## Questions:

* Should the `build`, `deploy`, `undeploy` scripts be scoped to a target cluster or not?
* Is local PVC okay for minikube "emulated" installation?
* Why the fuck am I doing this when I could just use VMs instead?
