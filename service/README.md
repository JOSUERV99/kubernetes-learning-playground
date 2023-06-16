Lessons

- If your label in deployments and service not matched, the service
won't be able to redirect traffic to the pods of your deployment
- Service is used to make available your pods in your kubernetes cluster
to the internet
- Other services type are NodePort and ClusterIp
- In local if you get services, the external ip is gonna be 127.0.0.1, if
we use any Kubernetes provider they will give you a public address on internet