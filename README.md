本项目只要存放工作中需要在K8S集群上部署的各种服务  
目前文件上传情况：    

|    名称    |单节点|高可用|
|:---:|:---:|:---:|  
|  MySQL   |&#10004;|&#10006;|
|  neo4j   |&#10004;|&#10006;|
|  Minio   |&#10004;|&#10006;| 
|  Redis   |&#10004;|&#10006;|
|  Nginx   |&#10004;|&#10006;|
| RabbitMQ |&#10004;|&#10006;|



使用方式：

1. 创建命名空间
```base
kubectl create namespace dev
```
2. 添加环境变量
```base
your_namespace=dev
```
3. 替换命名空间
```base
sed -i 's/guoyun/$your_namespace/g' k8s/mysql/mysql.yaml
```
4. 导入K8S
```base
kubectl apply -f k8s/mysql/mysql.yaml
```