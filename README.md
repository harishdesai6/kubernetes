# kubernetes
DaemonSets in Kubernetes Cluster

Like other controllers, DaemonSets manage groups of replicated Pods.

However, DaemonSet ensures that all or selected Worker Nodes run a copy of a Pod (one-Pod-per-node).

As you add nodes, DaemonSets automatically add Pods to the new nodes. As the nodes are removed from the cluster, those Pods are garbage collected.

Check the pods created 
" kubectl get pods -n kube-system "

Check number of nodes
" kubectl get nodes "

Display Daemonset
" kubectl get daemonsets "

details of Daemonsets
" kubectl describe daemonset fluentd "

daemonset
"kubectl delete daemonset fluentd "

Uses of daemonset
running a cluster storage daemon, such as glusterd, ceph, on each node.

running a logs collection daemon on every node, such as fluentd or logstash.

running a node monitoring daemon on every node, such as Prometheus Node Exporter, AppDynamics Agent, Datadog agent, New Relic agent, etc.

## Deployment

While pods are the unit of deployment. For an application to work, it needs one or more pods. Kubernetes considers this entire set as deployment.

Thus deployment is recorded information about pods. Kubernetes uses this deployment information to manage and monitor the applications that are deployed in them.

After yaml fil;e written use the below command to run the file,
"kubectl apply -f fgfdeploy.yaml"

## Service 
The deployments define the actual state of the application running on the containers. Users will need to access the application or you might need to connect to the container to debug it. Services will help you.

The services are the Kubernetes object that provides access to the containers from the external world or between themselves.

After service is deployed run the below command,
"kubectl apply -f gf-svces.yaml"

## statefulset

Often times we will need to have persistent storage or permanent network identifiers or ordered deployment, scaling, and update. During those times we will use StatefulSets.
