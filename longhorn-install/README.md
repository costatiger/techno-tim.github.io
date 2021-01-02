# Cloud Native Distributed Storage in Kubernetes with Longhorn


[![Cloud Native Distributed Storage in Kubernetes with Longhorn](https://img.youtube.com/vi/eKBBHc0t7bc/0.jpg)](https://www.youtube.com/watch?v=eKBBHc0t7bc "Cloud Native Distributed Storage in Kubernetes with Longhorn")


Storage in Kubernetes is hard, complicated, and messy.  Configuring volumes, mounts, and persistent volumes claims and getting it right can be a challenge.  It's also challenging to manage that storage, replicated it across all your Kubernetes clusters.  It's also been very challenging to do this on bare metal, outside of a cloud provider.  That's where Longhorn comes.  Longhorn is an open source, a CNCF distributed block storage system for Kubernetes.  It comes with a UI, backups, snapshots, and cluster disaster recovery and it does all this with or without Rancher.  Rancher is NOT a requirement.



https://www.youtube.com/watch?v=eKBBHc0t7bc


## install

### Rancher app catalog

See the app catalog within Rancher



### kubectl


```
kubectl apply -f https://raw.githubusercontent.com/longhorn/longhorn/master/deploy/longhorn.yaml
```


```
kubectl get pods \
--namespace longhorn-system \
--watch

```

See more at https://longhorn.io/docs/1.0.0/deploy/install/install-with-kubectl/


### helm

helm3

```
kubectl create namespace longhorn-system
helm install longhorn ./longhorn/chart/ --namespace longhorn-system
```

```
kubectl -n longhorn-system get pod
```