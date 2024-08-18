# Multi-container commands
kubectl exec -it multi-container-pod -c logger-container -- /bin/sh

kubectl exec -it multi-container-pod -c nginx-container -- /bin/bash

# container log
kubectl logs multi-container-pod -c nginx-container

kubectl logs multi-container-pod -c logger-container

# etcd command

sudo ETCDCTL_API=3 etcdctl --endpoints $advertise_url --cacert /etc/kubernetes/pki/etcd/ca.crt --key /etc/kubernetes/pki/etcd/server.key --cert /etc/kubernetes/pki/etcd/server.crt --write-out=table snapshot status etcd_backup.db
