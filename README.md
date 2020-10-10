# kubernetes101

## Important commands:

### PODS
```
kubectl get pods
kubectl run nginx --image=nginx 
kubectl describe pod <PODNAME> | grep -i image 
kubectl get pods -o wide
kubectl delete pod <POD_NAME>
kubectl delete pods --all 
kubectl run redis --image=redis123 --dry-run=client -o yaml > pod.yaml
kubectl apply -f <ymlFileName>
kubectl create -f <fileName>
```

### ReplicaSets

1. Replicaset and relplica controllers are responsible for the same task: ensuring the number of pod running at a time.
2. Difference between them 
    * `apiVersion: v1` for replicationController and `apiVersion: apps/v1` for ReplicaSet 
    * ReplicaSet require `selector` property because it can also manage other pod which is not being created along with Replicaset

```
kubectl apply -f <fileName>
kubectl scale --replicas=6 -f replicaset-definition.yaml
kubectl scale --replicas=6 replicaset my-app-replicaset
                           ||<type>||    ||<name>||


```



