### Kubernetes go app.

This deploys the sample go application into a kubernetes cluster.


## Prerequisites.
1. Kubernetes cluster running atleast 1.15.
2. (Optional) Some Cloud account if you need to run on any cloud provider behind a loadbalancer. 

## Steps
1. Run `kubectl apply -f .` to deploy the application to a kubernetes cluster.
2. Once done the same can be accessed using the load balancer ip/Node ip:exposed port.
3. The respective Deployment/Stateful set can be scaled by `kubectl scale --replicas=n -f <resourcefile.yaml` or `kubectl scale --replicas=3 <resource/resourcename>`.