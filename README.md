# K8S_the_hardway

Bootstrapping the etcd Cluster

after downloading the tar file and unzip it, you can execute the etcd binary code 

wget "https://github.com/etcd-io/etcd/releases/download/v3.4.10/etcd-v3.4.10-linux-amd64.tar.gz"
./etcd --listen-client-urls=http://127.0.0.1:8888 --advertise-client-urls=http://127.0.0.1:8888
