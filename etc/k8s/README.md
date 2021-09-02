 ### Pre-requirements

* Docker Desktop with Kubernetes enabled
* Install [NGINX ingress](https://kubernetes.github.io/ingress-nginx/deploy/) for k8s

### How to run?

* Add entries to the hosts file (in Windows: `C:\Windows\System32\drivers\etc\hosts`):

````
127.0.0.1 eh-st-account
127.0.0.1 eh-st-www
127.0.0.1 eh-st-api
127.0.0.1 eh-st-admin
127.0.0.1 eh-st-admin-api
````

* Run `build-images.ps1` in the `scripts` directory.
* Run `deploy-staging.ps1` in the `helm-chart` directory. It is deployed with the `eventhub` namespace.
* *You may wait ~30 seconds on first run for preparing the database*.
* Browse https://eh-st-www and https://eh-st-admin
* Username: `admin`, password: `1q2w3E*`.