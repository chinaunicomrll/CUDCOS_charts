# CUDCOS_charts
Helm使用Chart来管理Kubernetes manifest文件。每个chart都至少包括

应用的基本信息Chart.yaml;
一个或多个Kubernetes manifest文件模版（放置于templates/目录中），可以包括Pod、Deployment、Service等各种Kubernetes资源;
```Bash
tree -L 2
.
├── Chart.yaml
├── charts
├── templates
│   ├── NOTES.txt
│   ├── _helpers.tpl
│   ├── configmap.yaml
│   ├── services.yaml
│   └── statefulset.yaml
└── values.yaml
```
Chart.yaml用于描述MySQL chart

templates/configmap.yaml用于生成MySQL配置文件

templates/services.yaml用来配置MySQL服务

templates/statefulset.yaml用来定义MySQL StatefulSet
