1. Create a ClusterRole named role1 that grants get and list permissions on pods and services across all namespaces.
2. Create a ClusterRoleBinding named role1-binding to assign role1 to a user named user1.
3. Create a user named user1(htpasswd) in OpenShift and configure the authentication.
4. Log in as user1 and verify if user can list pods and services in any namespace.
5. Try listing deployments as user1 and confirm whether access is granted or denied.
6. Modify role1 to include watch permission for deployments and verify if user1 can now watch deployments.
7. Delete role1 and role1-binding and confirm that user1 no longer has access.
