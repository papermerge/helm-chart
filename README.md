# Helm Chart for Papermerge

This is helm chart for Papermerge deployment in Kubernetes cluster.


## Install

In order to install papermerge use following command:

    helm install papermerge . -f .values.yaml

Example of .values.yaml:

    global:
      conf:
        ingress:
          host: papermerge.minikube
        db:
          host: "pg-postgresql"
        redis:
          host: "redis-master"
      secrets:
        db:
          password: "<hidden>"
        app:
          secret_key: "<hidden>"
          superuser:
            password: "<hidden>"
