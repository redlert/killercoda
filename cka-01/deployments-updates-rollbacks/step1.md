An application is deployed with the `kubectl create deployment` command. Kubectl is a command line tool that communicates with Kubernetes.

With the `kubectl create deployment` command, Kubernetes deploys an image that is executed in the command. Below, you will run an image of the Nginx web server application, with the command, `kubectl create deployment --image nginx my-nginx`. The command will deploy the image that is stored in the registry URL, docker.io/nginx/nginx, since Kubernetes uses the Docker Hub by default.

Deploy an application image of the Nginx web server named "my-nginx" with the following command, `kubectl create deployment --image nginx my-nginx --port=8080`{{execute}}

Verify the deployment with the following command:
`kubectl get deployments`{{execute}}

For a more detailed description of the application, run the following command:
`kubectl describe deployments`{{execute}}
