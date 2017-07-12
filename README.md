# CUDCOS_charts
CU-DC/OS使用Helm工具操作镜像

Helm工具使用Chart来管理Kubernetes manifest文件。每个chart都至少包括

应用的基本信息Chart.yaml;

一个或多个Kubernetes manifest文件模版（放置于templates/目录中），可以包括Pod、Deployment、Service等各种Kubernetes资源;


##以mysql模板为例说明charts结构

```Bash
tree -L 2
.
├── Chart.yaml            用于描述MySQL chart
├── charts
├── templates
│   ├── NOTES.txt
│   ├── _helpers.tpl
│   ├── configmap.yaml    用于生成MySQL配置文件
│   ├── services.yaml     用来配置MySQL服务
│   └── statefulset.yaml  用来定义MySQL StatefulSet
└── values.yaml
```
