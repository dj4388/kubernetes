# Go through these docs to start the instalation

https://kind.sigs.k8s.io/docs/user/quick-start/
https://kubernetes.io/docs/tasks/tools/


# To install kind On Linux:

curl -Lo ./kind https://kind.sigs.k8s.io/dl/v0.17.0/kind-linux-amd64
chmod +x ./kind
sudo mv ./kind /usr/local/bin/kind

# To install kubectl on Linux:
https://kubernetes.io/docs/tasks/tools/install-kubectl-linux/

curl -LO "https://dl.k8s.io/release/$(curl -L -s https://dl.k8s.io/release/stable.txt)/bin/linux/amd64/kubectl"

sudo install -o root -g root -m 0755 kubectl /usr/local/bin/kubectl

# To check kubectl version
kubectl version --client --output=yaml

# Create a cluster using kind
kind create cluster

# For calculating total disk space you can use
kubectl describe nodes

# To see all the running pods
kubectl get pods -A