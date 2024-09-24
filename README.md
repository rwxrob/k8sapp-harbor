# K8SAPP: Harbor HA with PostgreSQL and Redis

This K8SAPP is a full HA Harbor installation. This installation follows one industry practices called K8SAPP for managing core enterprise applications.

The tricky part with installing Harbor HA is all the dependencies. The following *major* applications have to be full installed and working before Harbor HA can 

* PostgreSQL
* Redis
* Vault (optional for secrets)

This K8SAPP considers the first two to be a part of this application with the same namespace. Vault, however, is assumed to have been already installed. (See [k8sapp-vault](https://github.com/rwxrob/k8sapp-vault) for ideas about that.)
