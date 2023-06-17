Lessons

- Deployment is the most common way to deploy containerized apps
- Manage the number of replicas running
- When you have a new version of your application
Kubernetes can keep the old version and creates the new one
and then removing the old pods (NO-DOWNTIME UPGRADE)

- Using DAEMONSET, used for daemon containers
    - One per node
    - Background process
    = collects metrics about the underline node and other pods in the node

- Using JOB: can create one or more pods 
    - Run until completion
    - Example: an application that you deploy in a test cluster
    that will generate a batch of data for the test framework