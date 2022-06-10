An annotation is a description of a pod.

To update a pod with an annotation, run the `kubectl annotate pods`{{execute}} command.

Run the following command to annotate the first pod: `kubectl annotate pods $(kubectl get pod -o jsonpath='{.items[0].metadata.name}') description='Front-End Nginx Web Application'`{{execute}}

To view the annotation, run the following command: `kubectl get pods $(kubectl get pod -o jsonpath='{.items[0].metadata.name}') -o yaml`{{execute}}
