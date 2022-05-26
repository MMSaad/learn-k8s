# Pods

- Pods are the smallest deployable units of computing that you can create and manage in Kubernetes.

- A Pod (as in a pod of whales or pea pod) is a group of one or more containers, with shared storage and network resources, and a specification for how to run the containers

## Sample Pod
> [sample](sample.yml)
```yml
apiVersion: v1
kind: Pod
metadata:
  name: nginx
spec:
  containers:
  - name: nginx
    image: nginx:1.14.2
    ports:
    - containerPort: 80
```


## Create pod
```
kubectl create -f sample.yml
```

## Pods with 2 containers that's shares storage volume
> [sample](pods-with-shared-volume.yml)
```yml
apiVersion: v1
kind: Pod
metadata:
  name: examplepod
  namespace: pod-example
spec:
  volumes:
    - name: html
      emptyDir: {}
  containers:
    - name: nginx
      image: nginx:1.14.2
      ports:
        - containerPort: 80
      volumeMounts:
        - name: html
          mountPath: /usr/share/nginx/html
    - name: filecontainer
      image: debian
      volumeMounts:
        - name: html
          mountPath: /html
      command: ["/bin/sh","-c"]
      args:
       - while true; do
          date >> /html/index.html
          sleep 1;
         done
```