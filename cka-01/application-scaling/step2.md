To scale the application down back to 3 replicas, run the command `kubectl scale deployment/$(kubectl get deployment -o jsonpath='{.items[0].metadata.name}') --replicas=3`{{execute}}

To verify that the number of replicas have been reduced, run the command `kubectl get pods`{{execute}}
