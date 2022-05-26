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

9. create replica set
```
kubectl apply/create -f ./file-name
```
10. get cluster replica set(s)
```
kubectl get rs
```
11. check the state of replica set
```
kubectl describe rs/{name}
```
12. scale replica set
```
kubectl scale rs/{name} --replicas=4
```
13. auto-scale replica set
```
kubectl autoscale rs frontend --max=10 --min=3 --cpu-percent=50
```
14. delete replica set
```
kubectl delete rs/{name}
```
15. list cluster services
```
kubectl get service
```
