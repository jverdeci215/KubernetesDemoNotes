#  ReadME

##  RBAC Files
-  [Service Account](./demo-sa.yaml)
-  [Clusterrole definition](./demo-cr.yaml)
-  [Clusterrolebinding definition](./demo-binding.yaml)

##  Storage Files
-  [Persistent Volume](./pv-demo.yaml)
-  [Persistent Volume Claim](./pvc-demo.yaml)
-  [Stateful Set](./ss-demo.yaml)

##  Pod Definition
-  [Pod](./demo-pod.yaml)


##  Ingress
1.  Install `helm`.

- **Windows:**
```
choco install kubernetes-helm
```

- **Mac/Linux:**
```
brew install helm
```

2.  Run the following command to add the ingress controller repo to helm:

```
helm repo add ingress-nginx https://kubernetes.github.io/ingress-nginx
```

3.  Run the following command to install the ingress controller:

```
helm install my-nginx ingress-nginx/ingress-nginx
```

4.  Copy and paste the code from [ingress.yaml](./ingress.yaml) to your local folder.

5.  Apply the file. *Hint: `kubectl apply -f ingress.yaml`*

6.  Add the following line to hosts file found at (C:\Windows\System32\drivers\etc\hosts) on windows or (/etc/hosts) on Mac/Linux:

```
127.0.0.1 ingress.local
```

- *Note: use an administrator terminal on windows*

7.  Open a web browser and head to `ingress.local`.

8.  Hopefully you see your site!

