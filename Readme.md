# Kubernetes

Kubernetes is an Orchestrator for Microservice apps
- Microservice apps = Lots of independent and small services that come together to create an app.

Kubernetes is built on linux

Uses Master and Nodes
- Master
    - Api server
        - Exposes a front end to the control plane
    - Cluster store
        - Cluster state and config
        - Runs on etcd
- Node
    - Minions
    - Where the work happens
    - Kublet - Manages the pods
    - Container Engine
        -   Docker or rkt
    - Kube-proxy
        -   Kubernetes networking

Work is sent to the cluster through an API server from a Manifest file
The master decides which nodes are to be used

The nodes run the apps in a pod

Every node has its own set of default system pods.

# Objects in the K8 API

## Pods
- Atomic unit of scheduling
## Replication controllers
- Scale pods, desired state
## Deployment
- RC + rolling updates, rollbacks
## Services
- stable network