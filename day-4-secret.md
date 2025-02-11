1. Create a secret with oc command with following details.
   - Create a project registry
   - In registry project create a generic secret with name creds
   - Use oc command to create this secret and add key value pair username with value user1 and another pair with key password and value redhat@123
   - Check oc command that secret is created in the registry project
   - Try to extract the secret.
2. Try to decode the secret created in 1 question.
3. Create a nginx pod and then attach the creds secret with pod as environment variable. username key should be attached to the registry_user environment
   and password key should be attached to the registry_password environment variable in the pod.
4. After creating the pod enter into the pod and then check if env variables are created inside the pod.
5. Create a certificate key file and cert file.
6. Create a TLS secret with name tls-secret in the registry project.
7. Link the TLS secret to the default service account in the registry project.
8. Create a docker registry secret with name docker-secret, which will have info of your registry URL, registry username and registry password.
9. Now link that docker-secret with the default service account in the registry project.
