# Helm Chart for Papermerge 3

Official Papermerge helm chart.
It is compatible with following versions of Papermerge:

- 3.2

## Install

In order to install papermerge use following command:

    helm install papermerge . -f .values.yaml -f secrets.yaml

You need to provider one values.yml file and one secrets.yml.

Example of values.yaml:

```yaml
  worker:
    replicaCount: 1

  global:
    conf:
      app:
        auth__username: "admin"
        auth__email: "admin@example.com"
      redis:
        url: "redis://redis:6379/0"
      ingress:
        enabled: true
        host: papermerge.minikube
```

Example of secrets:

```yaml
global:
  secrets:
    app:
      security__secret_key: 123abc
      auth__password: 123abc
```
