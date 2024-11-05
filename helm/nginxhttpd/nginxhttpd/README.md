
```bash
$ helm create nginxhttpd
$ cd nginxhttpd
$ helm install my-release-2 .
$ helm install my-release-1 .
$ helm get manifest my-release-1
# $ helm install -f values-coffee.yaml coffee .

$ helm search repo nginx
$ helm repo add bitnami https://charts.bitnami.com/bitnami
$ helm search repo bitnami
$ helm search repo nginx
```