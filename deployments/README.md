Lessons

- To delete a pod from the cluster, you must delete the deployment first
- If you delete a pod, but no their deployment, is gonna be initialized right away again
- The thinking of Kubernetes cluster is to mantain the deployment alive, if one of them
 goes down, he will start a new pod inmediately
- There are namespaces and general namespace, be careful where to delete