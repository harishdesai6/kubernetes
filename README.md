# kubernetes Daemonset
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
