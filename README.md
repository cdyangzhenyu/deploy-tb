按照编排文件的文件名顺序创建各个 k8s 资源。在创建之前，应该检查每个编排文件内容，以确保符合特定的集群环境。

```bash
for resource in $(ls *.yaml); do kubectl create -f $resource; done
```
检查服务是否启动
```bash
kubectl -n thingsboard get all
```
