# learn-k8s

## Cluster diagram
![](cluster.png)

## Terminology 
- Kubelet
    - The kubelet is the primary "node agent" that runs on each node. It can register the node with the apiserver using one of: the hostname; a flag to override the hostname; or specific logic for a cloud provider.
- kubectl
    - k8s command line tool
- kubeadm
    - Kubeadm is a tool built to provide kubeadm init and kubeadm join as best-practice "fast paths" for creating Kubernetes clusters
- etcd
    - etcd is a strongly consistent, distributed key-value store that provides a reliable way to store data that needs to be accessed by a distributed system or cluster of machines. It gracefully handles leader elections during network partitions and can tolerate machine failure, even in the leader node
- API server
    - The API server is a component of the Kubernetes control plane that exposes the Kubernetes API. The API server is the front end for the Kubernetes control plane
- kube-scheduler
     - Control plane component that watches for newly created Pods with no assigned node, and selects a node for them to run on
- kube-controller-managerLINK
    - Control plane component that runs controller processes
- kube-proxy
    - kube-proxy is a network proxy that runs on each node in your cluster, implementing part of the Kubernetes Service concept
- Container Runtime
    - The container runtime is the software that is responsible for running containers


## Lessons
- [Launch a k8s cluster](/lessons/install/index.md)
- [Basic commands](/lessons/basic-commands/index.md)
- [Pods](/lessons/pods/index.md)
- [ReplicaSet](/lessons/replica-set/index.md)
- [Services](/lessons/services/index.md)
- [Deployments](/lessons/deployments/index.md)