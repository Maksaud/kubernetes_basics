# Working with pods

## Atomic Unit of scheduling compared to other stuff
- Hypervisor/Virtualisation
    - Virtual Machines!!

- Docker
    - Container

- Kubernetes
    - Pod

## Pods
- A pod contains one or more containers
- A pod is deployed to a cluster by being defined in a manifest file
- Feed the manifest file to the apiserver
- The scheduler deploys it to a node
- The pod gets a single IP, not the containers
    - Every container inside the pod shares a single namespace

## Inter-pod communication
- All pod addresses are fully routable on the pod network
- Every pod gets its own IP that is routable on that network
- Every pod can talk directly to every other pod

## Intra-pod communication
- All the containers inside the pod communicate with eachother from localhost
- If each of the containers need to be shared outside, then you must expose them on ports

## Atomic deployment
- The containers will turn on and then the pod itself or the containers dont and the pod fails
- There is no such thing as a half working pod
- A pod can only be deployed in a single node

## Lifecycle.
- A pod gets defined in a manifest file
- Manifest is thrown to the apiserver and gets scheduled to a node
- it goes into a pending state
- Until all containers are up, it stays in the pending state
- Running state.
- Shuts down and changes to succeeded
- It could be in the failed state
- Pods are cattle and are replaced easily.