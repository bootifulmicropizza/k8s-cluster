# Kubernete Cluster Configuration

To create:

```
$ export $K8S_CLUSTER_NAME=k8s.bootifulmicropizza.com
$ kops create -f cluster.yaml --name $K8S_CLUSTER_NAME
$ kops create secret --name $K8S_CLUSTER_NAME sshpublickey admin -i ~/.ssh/id_rsa.pub
$ kops update cluster --name $K8S_CLUSTER_NAME --yes
$ kops validate cluster
```

Any subsequent update can be applied to the cluster using the replace command:

```
$ kops replace -f cluster.yaml --name $K8S_CLUSTER_NAME
```
