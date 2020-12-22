# Installing Kubernetes

## Minikube
- Ideal for: Local dev environments
- Laptop/desktop installs
- NOT for production

Minikube spins up a vm and runs a small kubernetes rig. Once you point your Kubectl client at it to get Minikube working.

## Google container Engine

Integrated with the Google Cloud and packaged kubernetes production grade.

## AWS with kops

Integrates with AWS

## Manual with kubeadm

bash```
kubeadm init
```

bash```
kubeadm join --token <token>
```


