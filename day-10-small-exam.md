# OpenShift Kubernetes Tasks

## Task List

### 1. Replace OpenShift API and Ingress Certificates
- Replace the default OpenShift API certificate with a custom certificate.
- Replace the OpenShift Ingress certificate with a custom certificate.

### 2. Create a Secret with a Password Variable and Attach it to a Pod
- Create a Kubernetes Secret named `postgres-secret` containing a password variable `POSTGRES_PASSWORD`. The password should be `redhat`
- Attach this secret to a pod named `postgres-pod` as an environment variable using the `postgres` image.

### 3. Create a ConfigMap with an Nginx Config File and Use it in a Pod
- Create a ConfigMap named `nginx-config` containing an `nginx.conf` file.
- Create a Pod named `nginx-pod` that mounts this ConfigMap and uses the custom configuration.

### 4. Create a Service Account and Use It
- Create a Kubernetes Service Account named `custom-sa`. Add the `view` role to the SA.
- Use the created Service Account in a Pod named `sa-pod`.

### 5. Expose Internal OpenShift Registry and Configure a User for Push/Pull Access
- Expose the internal OpenShift Container Registry.
- Create a user named `registry-user` and grant him access to push and pull images in the OpenShift registry.

### 6. Import OpenShift Ingress Certificate on a Podman System and Push an Image
- Extract the ingress certificate and then import the OpenShift ingress certificate on a system with `podman` installed.
- Push an image named `custom-image` to the OpenShift registry from a Podman system.

### 7. Create a Custom Role with Specific Permissions
- Create a Kubernetes custom role named `custom-viewer-role` that grants `get`, `list`, and `watch` permissions for Deployments, Pods, ReplicaSets, Services, and Routes.

### 8. Create a Docker Secret to Push Images from a Private Registry
- Create a Kubernetes secret named `docker-registry-secret` for authentication with a private Docker registry.
- Use this secret to pull an image named `private-app` from the private registry onto a Kubernetes cluster.

