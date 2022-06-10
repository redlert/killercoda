In the home directory, there is a YAML file that deploys an Nginx web application.

To view the YAML file, run the `ls ~/`{{execute}} command.

To view the contents of the YAML file, run the `cat ~/deployment.yml`{{execute}} command.

If you view the contents of the YAML file, you will see that the application was deployed with a scale of 3 replicas.

To deploy YAML file, run the `kubectl apply -f ~/deployment.yml`{{execute}} command.

To scale the application up to 6 replicas, run the command `kubectl scale deployment/$(kubectl get deployment -o jsonpath='{.items[0].metadata.name}') --replicas=6`{{execute}}

To view the new replicas, run the command `kubectl get pods`{{execute}}
