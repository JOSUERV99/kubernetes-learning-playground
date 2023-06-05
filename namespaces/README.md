Lessons

- Pods are created dby defining the replicas attribute in deployment files
- Namespaces are used to group deployments by subject, for example development or production
- You can delete pods with delete pod and using -n to specify which namespace
- Deployments creates pods by the replica configuration, using the docker container maps from yml config file
- Yml or yamls as extension are allowed, better if we use tools to verify that the spacing is correct in our config files