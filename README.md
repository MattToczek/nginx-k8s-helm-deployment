# Helm K8s GCP Nginx Basic Deployment

### Description
This is a basic deployment of an nginx server onto GCP using K8s and Helm. GCP is used for the ingress controller, otherwise the deployment is cloud agnostic.

### Deployment
Configure a GKS cluster (using Autopilot is the simplest way for this deployment) 

Configure your local machine or an CI/CD tool to target the cluster using:
`gcloud config set project <PROJECT_NAME>`
`gcloud container clusters get-credentials <CLUSTER_NAME> --region <REGION>`

Deploy to your cluster from the root dir of this repo using Helm: 
`helm install . --values ./<ENV_FILE>` 

Where `<ENV_FILE>` refers to the values files `prod.yaml` or `dev.yaml`
