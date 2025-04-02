1. `kubectl create serviceaccount <name> -n <name>
2. Role
3. RoleBinding
4. Create token using ServiceAccount
   `kubectl get secret $(kubectl get serviceaccount default -n <your-namespace> -o jsonpath="{.secrets[0].name}") -n <your-namespace> -o jsonpath="{.data.token}" | base64 --decode`
