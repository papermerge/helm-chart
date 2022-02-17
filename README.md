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
