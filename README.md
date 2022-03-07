# open5gs

### Install Kubernetes Cluster

### Install Linkerd

### Clone open5gs helm
```bash
git clone https://bitbucket.org/infinitydon/opensource-5g-core-service-mesh.git
```

**Note:** The helm chart is simple, you can leave the default values as it is or change some of the parameters like mnc, mcc etc.

### Install the open5gs 5G core

Create the namespace with linkerd auto injection
```bash
kubectl create -f namespace.yaml
```
Install open5gs 5G helm chart
```bash
helm -n open5gs install -f values.yaml open5gs ./
```

### Access Open5gs UI

**Note:** change svc of web-ui from ClusterIP to NodePort

```bash
kubectl port-forward -n open5gs podName 3000
ssh -L localhost:3000:localhost:3000 ubuntu@192.168.5.97
```

#### Open Browser
Visit localhost:3000
**user** - admin 
**password** - 1423
