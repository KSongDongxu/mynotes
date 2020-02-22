#Kubernetes API 资源应该使用哪个 Group 和 Version?

####获取 Kubernetes集群支持的所有 API 资源

>kubectl api-resources -o wide

+ SHORTNAMES 资源名称简写
+ APIGROUP => apiVersion
+ KIND 资源类型
+ VERBS 可用的方法

**获取特定 API 组的 API 资源**

> kubectl api-resources --api-group apps -o wide

#### 使用kubectl explain命令获取有关资源的详细信息

> kubectl explain configmap

**需要注意的是 explain命令可能会显示旧的 group/version，我们可以通过 –api-version参数显示设置它**

> kubectl explain replicaset --api-version apps/v1

 #### 获取集群支持的所有API版本

> kubectl api-versions

**检查特定的 group/version是否可以用于某些资源**

> kubectl get deployments.v1.apps -n kube-system



详情参考：[Kubernetes API 资源应该使用哪个 Group 和 Version?]([http://liupeng0518.github.io/2018/12/24/k8s/%E6%A6%82%E5%BF%B5/%E5%A3%B0%E6%98%8E%E5%BC%8FAPI/Kubernetes_API%E8%B5%84%E6%BA%90%E7%9A%84Group%E5%92%8CVersion%E9%80%89%E6%8B%A9/](http://liupeng0518.github.io/2018/12/24/k8s/概念/声明式API/Kubernetes_API资源的Group和Version选择/))

