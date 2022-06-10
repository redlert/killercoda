Labels help organize resources and make them easier to access, review and troubleshoot.

Examples of labels:
  app
  tier
  role

Examples of label values:
  app: nginx, apache
  tier: frontend, backend
  role: master, worker

Given that we deployed an Nginx application, the label would be "nginx".
Nginx is a front-end web application, so the tier would be "frontend".
It is run in the sector of the Kubernetes architecture that is run by other components such as the API server, so the role would be "worker".

To view the pods, run the command: `kubectl get pods`{{execute}}.

To label the first pod, `kubectl label pods $(kubectl get pod -o jsonpath='{.items[0].metadata.name}') app=nginx tier=frontend role=worker`{{execute}}

To review the labels, run the command: `kubectl get pods -l app=nginx tier=frontend role=worker`{{execute}}
