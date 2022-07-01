# Install kind

insatll Kubectl  

```
curl -LO https://storage.googleapis.com/kubernetes-release/release/v1.22.6/bin/linux/amd64/kubectl
chmod +x ./kubectl
sudo mv ./kubectl /usr/local/bin/kubectl
```{{execute}}


install kind
```
curl -Lo ./kind https://github.com/kubernetes-sigs/kind/releases/download/v0.11.1/kind-linux-amd64  
chmod +x ./kind  
mv ./kind /usr/local/bin/kind
```{{execute}}  


create cluster  
`kind create cluster --name my-cluster`{{execute}}

`export KUBECONFIG="$(kind get kubeconfig-path --name="my-cluster")"`{{execute}}

`kubectl get nodes`{{execute}}
