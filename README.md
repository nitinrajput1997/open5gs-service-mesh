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

