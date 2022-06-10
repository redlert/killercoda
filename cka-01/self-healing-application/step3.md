A DaemonSet makes sure that all or some Nodes run a copy of a Pod. As nodes are added to the cluster, Pods are added to them. As nodes are removed from the cluster, those Pods are garbage collected.

To view the YAML file that deploys a DaemonSet, run the command: `cat ~/daemonset.yml`{{execute}}

To deploy the file, run the command: `kubectl apply -f ~/daemonset.yml`{{execute}}

To view the DaemonSet, run the command: `kubectl describe daemonset fluentd-elasticsearch -n kube-system`{{execute}}
