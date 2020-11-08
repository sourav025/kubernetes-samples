# kubernetes-samples
## Required Tools
  1. Kubernetes cluster (minikube)
  2. Kubectl
  3. Kubectx

## To run ingress on minikube 
Install minikube addon ingress using
```
minikube addon enable ingress
```
## How to check ingress on minikube
- Deploy `nginx-service`
- Use `kubectl get ingress` to find the Address IP (eg. `192.168.64.3`)
- Append `192.168.64.3 mylocal.com` to your `/etc/hosts`
- Open the browser and hit `mylocal.com`
- Nginx service should pop up

## Handle DNS name in GCE and K8s Ingress

- Create Zone in GC DNS
- Create static IP using gcloud
- Add RecordSet entry to GC DNS
- Create Server with LoadBalancer/NodePort + Proper Deployment/POD
- PUT IP name in ingress annotation, gcloud example is tested with nginx
