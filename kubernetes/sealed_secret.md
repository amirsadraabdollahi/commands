# sealed secret

here some commands to apply sealed secrets in kubernetes

1. first get the original secret from kubernetes
```commandline
kubectl -n <namespace> get secret <secret_name> -o yaml > original-secret.yaml
```
2. second create the SealedSecret object from the original-secret.yaml
```commandline
cat original-secret.yaml | kubeseal --format yaml > sealed-secret.yaml
```
3. delete the original secret
```commandline
kubectl -n <namespace> delete secret <secret_name>
```
4. apply sealed-secret.yaml
```commandline
kubectl -n <namespace> apply -f sealed-secret.yaml
```
The sealed secret controller on your kubernetes cluster do the rest.
It creates the secret object as the previous original secret. 
