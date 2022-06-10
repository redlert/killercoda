To have the system automatically choose the number of nginx replicas as needed, ranging from 1 to 6, run the command: `kubectl autoscale deployment/$(kubectl get deployment -o jsonpath='{.items[0].metadata.name}') --min=1 --max=6`{{execute}}

To view the autoscaling, run the command `kubectl get pods`{{execute}}
