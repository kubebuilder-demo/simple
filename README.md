# simple
一个Kubebuilder的简单demo
# 注意点
- go和docker镜像有些可能被qiang这块要处理
- Dockerfile golang builder 时要加 ENV GOPROXY="https://goproxy.cn,direct"
- Dockerfile 里的 gcr.io/distroless/static:nonroot 镜像被qiang了，改为：devk8s/gcr-io_distroless_static:nonroot
- config/default/manager_auth_proxy_patch.yaml下的 gcr.io/kubebuilder/kube-rbac-proxy:v0.13.1 改为 devk8s/gcr-io_kubebuilder_kube-rbac-proxy:v0.13.1
- 如果在苹果芯片上build用make docker-buildx（多平台build）