k8s concept by SS 
===
使用docker desktop with k8s build

下圖為Docker Desktop Kubernets設定<br>
![docker_desktop_k8s](image\docker_desktop_k8s.png)

開啟後再下方顯示Cluster資訊為single-node

回到Containers頁面可以看到多出很多k8s service 容器

![container_k8s](image\container_k8s.png)
 
這時可以使用以下指令 <br>
kubectl get node  #檢查node <br>
kubectl get pod -A #檢查pod <br>
kubectl get service #檢查service <br>