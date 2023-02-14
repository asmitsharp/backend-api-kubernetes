# backend-api-kubernetes
Deploy a REST API in Kubernetes

In this project I have deployed a REST API in localhost using Kubernetes.

In this I have used different kubernetes components such as :
- Deploy
- Services
- Ingress

I have use k3s for setting up local kubernetes cluster beacuse of lightweight installation.
 <p><i><b>curl -s https://raw.githubusercontent.com/rancher/k3d/main/install.sh | bash</b></i></p>
 
Also i have mapped port 80 from machine port to port 80 on k3s load-balancer because of ingress.
<p><i><b>k3d cluster create test -p "80:80@loadbalancer"</b></i></p>

Once the pod is running, the API is accessible within the cluster only. One quick way to verify 
the deployment from our localhost is by doing port forwarding:
  <p><i><b>kubectl port-forward my-backend-api-84bb9d79fc-m9ddn 3000:80</b></i></p>
  
