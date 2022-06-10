To rollback an application means to undo the update of an application. To do this, run the `kubectl rollout undo` command.

Run the `kubectl rollout undo deployments/my-nginx`{{execute}} command to rollback the update of the Nginx application.

Run `kubectl rollout status deployments/my-nginx`{{execute}} to check status of the rollback.
