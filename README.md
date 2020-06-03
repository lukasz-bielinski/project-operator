# project-operator
## build
    operator-sdk build lukaszbielinski/operator
## deploy
    kubectl apply -R -f deploy/

## to create ns cr should be created:

```
apiVersion: project.xddevelopment.com/v1alpha1
kind: Project
metadata:
  name: example-cr
spec:
  # Add fields here
  size: 3
  resourcequotarequestscpu: "7"
  resourcequotarequestsmemory: 7Gi
  resourcequotalimitscpu: "70"
  resourcequotalimitsmemory: 70Gi
  resourcequotacountjobsbatch: 70k
  resourcequotacountingresses: 7k
  resourcequotapods: 7k
  resourcequotaservices: "6000"
```  
