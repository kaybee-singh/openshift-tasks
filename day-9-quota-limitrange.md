# Kubernetes Resource Management - Exam Questions

## Namespace Setup
- Use the namespace **`resource-management`** for all tasks. If it does not exist, create it.

## Pod Resource Management
### 1. Create a Pod with Resource Requests and Limits
- Create a pod named **`limited-pod`** in the `resource-management` namespace with the following specifications:
  - CPU request: `250m`, Memory request: `256Mi`
  - CPU limit: `500m`, Memory limit: `512Mi`

### 2. Verify Pod Resource Requests and Limits
- Verify that the pod **`limited-pod`** has the correct resource requests and limits applied.

## LimitRange Configuration
### 3. Create a `LimitRange` for Default Resource Limits
- Create a `LimitRange` named **`container-limits`** in the `resource-management` namespace with the following:
  - Default request: CPU `200m`, Memory `128Mi`
  - Default limit: CPU `1`, Memory `1Gi`
  - Minimum resources: CPU `100m`, Memory `64Mi`
  - Maximum resources: CPU `2`, Memory `2Gi`

### 4. Verify the `LimitRange`
- Verify that the `LimitRange` **`container-limits`** is correctly applied in the `resource-management` namespace.

### 5. Test `LimitRange` by Creating a Pod Without Resource Requests
- Create a pod named **`default-limit-pod`** in the `resource-management` namespace **without specifying any resource requests or limits** and check if the default values from `LimitRange` are applied automatically.

## Resource Quota Configuration
### 6. Set a `ResourceQuota` for the Namespace
- Configure a `ResourceQuota` named **`namespace-quota`** in the `resource-management` namespace with the following constraints:
  - Maximum CPU requests: `2`
  - Maximum memory requests: `4Gi`
  - Maximum CPU limits: `4`
  - Maximum memory limits: `8Gi`
  - Maximum number of pods: `4`
  - Maximum number of secrets: `4`

### 7. Verify the `ResourceQuota`
- Verify that the `ResourceQuota` **`namespace-quota`** is correctly applied in the `resource-management` namespace.

### 8. Test the Quota by Creating 4 Pods
- Try creating **4 pods** (`quota-test-pod-1`, `quota-test-pod-2`, `quota-test-pod-3`, `quota-test-pod-4`) and confirm that the quota prevents a **5th pod** from being created.

### 9. Test the Secret Quota by Creating 4 Secrets
- Try creating **4 secrets** (`test-secret-1`, `test-secret-2`, `test-secret-3`, `test-secret-4`) and confirm that the quota prevents a **5th secret** from being created.

