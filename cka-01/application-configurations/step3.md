To update the labels of the first pod, `kubectl label pods $(kubectl get pod -o jsonpath='{.items[0].metadata.name}') app=apache tier=backend role=master --overwrite`{{execute}}

To review the labels, run the command: `kubectl get pods -l app=apache tier=backend role=master`{{execute}}
