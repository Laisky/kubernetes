# k8s with 100yrs certs


## Build

> prebuild binary: <https://s3.laisky.com/static/k8s/v1.25.4/kubeadm>

```sh
sudo apt install -y build-essential
make all WHAT=cmd/kubeadm GOFLAGS=-v
```

- `_output/bin/kubeadm`
