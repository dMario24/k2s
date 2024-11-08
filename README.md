# CMD

### READY
- run dashboard
```bash
$ minikube addons list
$ minikube addons enable metrics-server
$ minikube addons enable dashboard
$ minikube addons list
$ minikube dashboard --url
```

```bash
# 배포 적용
$ kubectl apply -f httpd-deployment.yaml
.
.
.
.
```

### helm
- https://helm.sh/docs/intro/cheatsheet/
```
$ mkdir -p pkg/nginx/
$ cd pkg/nginx/
$ helm create ngpd
$ rm -rf ngpd/templates/*
$ copy $CODE_HOME/*.yaml ngpd/templates/
$ helm install cnp ngpd/
$ helm list
NAME    NAMESPACE       REVISION        UPDATED                                 STATUS          CHART           APP VERSION
cnp     default         1               2024-11-08 10:31:33.377319879 +0900 KST deployed        ngpd-0.1.0      1.16.0
$ helm status cnp
NAME: cnp
LAST DEPLOYED: Fri Nov  8 10:31:33 2024
NAMESPACE: default
STATUS: deployed
REVISION: 1
TEST SUITE: None
$ helm history cnp
REVISION        UPDATED                         STATUS          CHART           APP VERSION     DESCRIPTION
1               Fri Nov  8 10:31:33 2024        deployed        ngpd-0.1.0      1.16.0          Install complete
```
