# Deploy KubeDB

Guide: [here](https://kubedb.com/docs/v0.13.0-rc.0/setup/install/)  <br>
Run this command to install KubeDB and its dependencies on your cluster:

```
curl -fsSL https://github.com/kubedb/installer/raw/v0.13.0-rc.0/deploy/kubedb.sh | bash
```

## RBAC on GKE

Run this command to enable RBAC for KubeDB on GKE:
```
kubectl create clusterrolebinding "cluster-admin-$(whoami)" \
  --clusterrole=cluster-admin \
  --user="$(gcloud config get-value core/account)"
```

## Deploy a Redis Cluster (sharded)

Guide: [here](https://kubedb.com/docs/v0.13.0-rc.0/guides/redis/clustering/redis-cluster/)

## Deploy a MySQL Cluster

Guide: [here](https://kubedb.com/docs/v0.13.0-rc.0/guides/mysql/clustering/group_replication_single_primary/)

## Deploy a MongoDB Cluster (sharded)

Guide: [here](https://kubedb.com/docs/v0.13.0-rc.0/guides/mongodb/clustering/sharding/)