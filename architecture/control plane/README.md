Lessons 

- Instance of Kubernetes is a cluster
    - Control plane
    - Worker node
- Is like an airport, cluster
    - Control plane is like a control tower, that had people that manage that all goes well
- Run (kubectl get pods -n kube-system) to look at the K core components

Control panel
- Kube API Server: expose Kubernetes API
Is the component that handles the most requests from the user and without the cluster cannot exist
    - Every element like pods, deployments, and the horizontal pod auto-scaler have API endpoints
    - Kubernetes API has a REST interface
    - kubectl and kubeadm are CLI tools to communicate with the K API via HTTP requests
    - To see every element that has API endpoints, run (kubect api-resources)
    - the API server is a containerized application

- etcd: opensource key-value storage and highly available
    - Save all data about the cluster state
    - Only the API server can communicate directly with etcd
    - Run as a pod and you can see logs to see how this work (kubectl logs etcd-minikube -n kube-system | jq)

- Kube scheduler: identifies newly created pods which don't have a worker node assigned yet
    - Also run as a pod
    - We can learn more by describing the pods or looking at the logs

- KubeControllerManager: is a loop that works continuously and checks the status of the cluster
    - Checks that all worker nodes are running properly, if something fails
    remove the worker node and replace it with a new one.
    - Create and check several lots of things in the cluster

- Cloud Provider API:
Allow connecting the cluster with a cloud provider
    - To use AWS, GCP, Azure, ... or any public cloud

All these components make Kubernetes a very popular orchestrator