# Jenkins Helm Chart
A basic helm chart for Jenkins on OpenShift 4.x with persistent volume enabled.

## Usage

- Clone the repository
- Install the helm chart

```bash
# Set the initial admin password
export ADMIN_PASSWORD=$(echo -n "password" | base64)
helm install jenkins --set admin_password=${ADMIN_PASSWORD} .
```
- To upgrade jenkins helm release

```bash
helm upgrade jenkins --set admin_password=${ADMIN_PASSWORD} .
```

- To delete jenkins instance

```bash
helm delete jenkins
```
## Notes

- If PVC storage is increased then pod must be restarted