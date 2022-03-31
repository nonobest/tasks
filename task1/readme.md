# Install k8s on linux
`curl -LO "https://dl.k8s.io/release/$(curl -L -s https://dl.k8s.io/release/stable.txt)/bin/linux/amd64/kubectl"`

# Instal K3D on linux
`wget -q -O - https://raw.githubusercontent.com/rancher/k3d/main/install.sh | bash`

# To create the cluster from config file

`k3d cluster create k3d-cluster --config k3d.config.yml`

# Export config to k8s
`k3d kubeconfig write k3d-cluster`

# Install the petclinic application using Yaml file
`kubectl apply -f petclinic.yaml`

# Install the Petclinic application using helm
`helm install petclinic task1`