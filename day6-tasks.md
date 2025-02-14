- Create a Deployment with 3 Replicas
   1. Create a deployment named myapp-deployment with 3 replicas using the nginx image.
   2. Create the deployment while specifying port 8080 for the container.
- Create a NodePort Service
   1. Expose the myapp-deployment as a NodePort service named myapp-service.
   2. Ensure that the service forwards traffic from port 8080 on the service to port 80 inside the container.
   3. Retrieve and check the assigned NodePort for the service.
- Expose the Service Using a Route
   1. Expose the myapp-service using an OpenShift route named myapp-route.
   2. Retrieve and check the external URL assigned to the route.
- Remove the kubeadmin user from the OpenShift cluster.
- Remove the self-provisioner role from the system:authenticated group so that normal users cannot create new projects.
- Create a Pod, Service, and Edge Route
   1. Create a pod named myapp-pod using the nginx image.
   2. Then create the service to expose the pod.
   3. Create an Edge route named myapp-route to expose the service externally.
   4. Retrieve the external URL assigned to the route and check if you are able to access the service by route URL.
- Create a ClusterIP Service and Access It from a Cluster Node
   1. Create a ClusterIP service named internal-service that exposes a pod running nginx on port 80.
   2. Retrieve the ClusterIP assigned to the service.
   3. Access the service with ClusterIP from a cluster node using oc debug and test connectivity with curl.
