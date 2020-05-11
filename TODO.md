Tekton

# Resources:
https://docs.nginx.com/nginx-ingress-controller/installation/installation-with-manifests/
https://www.arthurkoziel.com/creating-ci-pipelines-with-tekton-part-2/

# Dependencies:

Ingress
    EventListener
        TriggerBindings
        TriggerTemplate
            PipelineRun
                Pipeline
                    Tasks 

# Dependencies - implementation:

Ingress
    EventListener & TriggerBindings
        TriggerTemplate (with PipelineRun)
                Pipeline
                    Tasks

# Installation

gcloud container clusters create --zone europe-west1-c --cluster-version=1.15.11-gke.12 tekton-demo

gcloud container clusters get-credentials --zone=europe-west1-c tekton-demo

alias ka='kubectl apply -f'

# install ingress
ka gke-nginx-lb-ingress.yaml
ka gke-nginx-lb-ingress.yaml

# install tekton triggers and pipeline controller
ka tekton-pipeline-controller.yaml
ka tekton-triggers-controller.yaml
