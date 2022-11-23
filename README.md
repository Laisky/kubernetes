# k8s with 100yrs certs


## Build

> prebuild binary: <https://s3.laisky.com/static/k8s/v1.25.4/kubeadm>

```sh
sudo apt install -y build-essential


make all WHAT=cmd/kubeadm GOFLAGS="-v -a" GOLDFLAGS="-w -extldflags '-static'" &
make all WHAT=cmd/kubectl GOFLAGS="-v -a" GOLDFLAGS="-w -extldflags '-static'" &
make all WHAT=cmd/kubelet GOFLAGS="-v -a" GOLDFLAGS="-w -extldflags '-static'" &
wait
```

- `_output/bin/kubeadm`
- `_output/bin/kubectl`
- `_output/bin/kubelet`

```sh
chmod +x _output/bin/kube*
cp -f _output/bin/kube* /usr/bin/.
```
