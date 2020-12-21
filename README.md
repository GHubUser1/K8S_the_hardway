# K8S_the_hardway

Bootstrapping the etcd Cluster

after downloading the tar file and unzip it, you can execute the etcd binary code 

wget "https://github.com/etcd-io/etcd/releases/download/v3.4.10/etcd-v3.4.10-linux-amd64.tar.gz"
./etcd --listen-client-urls=http://127.0.0.1:8888 --advertise-client-urls=http://127.0.0.1:8888

Bootstrapping Kubernetes apiserver

download the kubernetes release binary :
wget "https://storage.googleapis.com/kubernetes-release/release/v1.18.6/bin/linux/amd64/kube-apiserver"

install the kubernetes binary
chmod +x kube-apiserver 

execute the binary code:
sudo ./kube-apiserver --etcd-servers=http://127.0.0.1:8888

Bootstrapping Kubernetes control manager

wget "https://storage.googleapis.com/kubernetes-release/release/v1.18.6/bin/linux/amd64/kube-controller-manager"

chmod +x  kube-controller-manager 

sudo ./kube-controller-manager --master=http://127.0.0.1:8080

Bootstrapping kubectl

wget "https://storage.googleapis.com/kubernetes-release/release/v1.18.6/bin/linux/amd64/kubectl"
chmod +x kubectl
./kubectl run test --image=nginx





