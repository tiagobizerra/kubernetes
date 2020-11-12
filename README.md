# Kubernetes
Repo to store k8s stuff
<br />

<br />

## kubectl Useful Commands
<br />

### Namespaces
#### get
```
kubectl get namespaces
```
#### describe
```
kubectl describe namespaces
```
<br />

### Pods
#### get
```
kubectl -n $NAMESPACE get pods
```
#### get wide (shows where each pod is)
```
kubectl -n rtf get pod -o wide
```
#### describe
```
kubectl -n $NAMESPACE describe pod $POD
```
#### logs (use -f option as tail)
```
kubectl -n $NAMESPACE logs $POD
```
#### yaml
```
kubectl -n $NAMESPACE get pod $POD -o yaml
```
### Cronjobs

#### Create a job from a cronjob
```
kubectl create job --from=cronjob/<name of cronjob> <name of job>
```
<br />

### Container
#### bash in container
```
kubectl -n sre exec -it my-pod --container main-app -- /bin/bash
```
