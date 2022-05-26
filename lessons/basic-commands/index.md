# Basic commands

1. Get Cluster nodes
```
kubectl get nodes
```

> can have wide view using flags -o wide

2. Get Cluster pods
> Get nodes in the default namespace
```
kubectl get pods
```
3. Get notes in all namespaces
```
kubectl get pods --all-namespaces
```

> filter result using | grep {text-to-filter-by}

4. get cluster namespaces
```
kubectl get namespaces
```

5. create a namespace
```
kubectl create namespace example
```

6. specify namespace for commands
```
kubectl --namespace=example get pods ...etc
```

7. delete pod
```
kubectl delete pod examplepod
```

8. create any object from file
```
kubectl create -f ./file-name
```

