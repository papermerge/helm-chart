# Helm Chart for Papermerge

This is helm chart for Papermerge deployment in Kubernetes cluster.


## Install

In order to install papermerge use following command:

  helm install papermerge . -f .values.yaml

Example of .values.yaml:

frontend:
  ingress:
    host: papermerge.minikube

apidocs:
  ingress:
    host: papermerge.minikube

backend:
  ingress:
    host: papermerge.minikube
  conf:
    superuser_username: "admin"
    superuser_email: "admin@example.com"
    superuser_password: "admin"
    db_type: "postgres"
    db_user: "postgres"
    db_name: "postgres"
    db_host: "pg-postgresql"
    db_password: "hidden"
    secret_key: "hidden"
    es:
      enabled: false
wsserver:
  ingress:
    host: papermerge.minikube
