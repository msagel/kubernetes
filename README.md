# Kubernetes Lab Commands Sheet 

###  Juju

| Command  | Description |
| ------------- | ------------- |
| `juju status`  | Reports the current status of the model, machines, applications and units   |
| `watch -c juju status --color`  | Track the deployment process live   |
| `juju deploy`  | Deploy a new application or bundle   |
| `juju add-unit `  | Adds one or more units to a deployed application.   |
| `juju add-credential`  | Adds or replaces credentials for a cloud, stored locally on this client  |
| `juju list-credentials`  | Lists locally stored credentials for a cloud   |
| `juju add-model`  | Adds a hosted model   |
| `juju list-models`  | Lists models a user can access on a controller   |
| `juju run-action`  | Queue an action for execution. E.g. `juju run-action kubernetes-worker/0 microbot replicas=5`   |


### Kubernetes 

| Command  | Description |
| ------------- | ------------- |
| `kubectl create -f [FILE/S]`  | creates resources from the given file, files, dir, url, [etc][2]  |
| `kubectl get pods`  | Lists all Pods. [`Viewing Finding Resourses`](#Viewing-Finding-Resourses)  |
| `kubectl get nodes`  | List all nodes, [`Viewing Finding Resourses`](#Viewing-Finding-Resourses)  |
| `kubectl get svc`  | List all services in the namespace |
| `kubectl get deploy`  | List deployments  |
| `kubectl get endpoints`  | List all endpoints  |
| `kubectl get ingress`  | List all ingress  |
| `kubectl get componentstatuses`  | Displays the health status of the components  |
| `kubectl get namespaces`  | Display namespaces  |
| `kubectl describe pod {POD_NAME}`  | Describes a specific pod  |
| `kubectl describe node {NODE_NAME}`  | Describes the status of a specific Node, CPU and memory (system information)  |
| `kubectl delete pod {POD_NAME}`  | deletes the specified pod  |
| `kubectl delete namespaces {NAMESPACE_NAME}`  | delete a specific namespace  |
| `kubectl delete deploy {DEPLOY_NAME}`  | deletes a specific deployment  |
| `kubectl expose deployment {DEPLOY_NAME} --type="ClusterIP"`  | exposes an external IP address  |
| `kubectl top node `  | Display Resource (CPU/Memory/Storage) usage of nodes  |

### Viewing Finding Resourses:
`kubectl get pods --all-namespaces` List all pods in all namespaces

`kubectl get pods -o wide` List all pods in the namespace, with more details
