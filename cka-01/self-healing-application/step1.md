A ReplicationController makes sure that a pod or a homogeneous set of pods is always up and available.
If there are too many pods, the ReplicationController terminates the extra pods. If there are too few, the ReplicationController starts more pods.

In the home directory, there is a YAML file that can deploy a ReplicationController. To view the it, run the command: `cat ~/replicationcontroller.yml`{{execute}}

To deploy the the file, run the command: `kubectl apply -f ~/replicationcontroller.yml`{{execute}}

To view the replicacontroller, run the command: `kubectl describe replicationcontrollers/nginx`{{execute}}

To view the pods that have been deployed by the replicaset, run the command: `kubectl get pods --selector=app=nginx --output=jsonpath={.items..metadata.name} && echo`{{execute}}
