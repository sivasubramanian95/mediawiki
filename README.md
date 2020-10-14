# Introduction
Deploy mediawiki on kubernetes cluster using helm chart.
Here Test deployment was done on k3s Civo Cloud.

# Prerequisite
- Kubernetes Cluster (version - 1.14+)
- Helm (version - 3)
- Nginx Ingress Controller installed (Traefik can also be used as civo k3s comes with traefik as default)

# Deployment Procedure
- pull the repo (git clone)
- Enter into the directory (cd mediawiki)
- Make changes on the values.yaml file as per your requirement.
- fetch the absolute_path for the current directory (pwd)
- execute helm ``helm install my-release absolute_path``

# For any New Feature

- Please use `helm upgrade` command for any feature.

  ex: `helm upgrade my-release absolute_path`

- You can view your releases using 
      `helm ls` 
- To rollback to your previous release,
      `helm rollback <RELEASE> 0`
- To Uninstall application,
      `helm delelte <RELEASE>`
