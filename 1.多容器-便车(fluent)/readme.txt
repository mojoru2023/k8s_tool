

1. k apply -f configmap.yaml

创建configmap

2.  用到了fluentd镜像 

k apply -f deployment.yaml



3. 验证第一个 容器的输出，第二个容器的读取

kubectl exec  deployment-web-5fcd48ffb5-ml6sf -c logger-123   -- tail /ckad/log/input.log


kubectl exec  deployment-web-5fcd48ffb5-ml6sf -c adopter-dev -- tail /ckad/log/input.log
