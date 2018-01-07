## install redis on a k8s cluster

```
kubectl create -f redis-master.yaml
kubectl create -f redis-sentinel-service.yaml
kubectl create -f redis-service.yaml
kubectl create -f redis-control.yaml
kubeclt scale rc redis-sentinel --replicas=3
kubeclt scale rc redis --replicas=3
kubectl delete pods redis-master
```
