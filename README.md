# [Backstage](https://backstage.io)

This is the newly scaffolded Backstage App!

To export all the env vars in .env file, run:
```shell
export $(xargs <.env)
```

To start the app, run:

```sh
yarn install
yarn dev
```

Configuring kubernets plugin:
1. Run k8s/crd.yaml
2. Run k8s/secret.yaml
3. To get token, run
```shell
   kubectl -n default get secret default-secret -o=json | jq -r '.data["token"]' | base64 --decode
```
4. To get k8s URL, run
```shell
   kubectl cluster-info
```
5. To enable metrics server to view CPU and memory utilization, run the following
```shell
   minikube addons enable metrics-server
```
6. Bring up prometheus and grafana
```shell
```