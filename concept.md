k8s concept by SS 
===
>以下出自於[Gcore](https://gcore.com/blog/top-10-container-orchestration-tools/)介紹 
<br>

目前已經有許多tools被用於迎合各種需求像是:simple to large-scale部屬、強化效率和可擴充性等等。<br>
Container orchestration tools基本用於管理container的lifecycle其中包含:networking, load balancing, and scaling等等。<br>
該網站會列出10種container orchestration tools並介紹這些tools的key components, capabilities, helping DevOps teams achieve application resilience(彈性), improved security and simplified operations.<br>

The importance of Container Orchestration
===
Containers容器化是一項革命化技術，透過複製environment,portability,resource efficiency, scalability and unmatched isolation capabilities 來幫助applications進行分散式。<br>
Container可以幫助我們包裝application來更容易的<font color="Blue">部屬和更新</font>因此我們需要一些特別的tools來管理這些container。<br>
Orchestration tools提供自動containerized workloads 一個框架，一些tools可以幫助開發團隊管理container的lifecycle以及implement container的networking、load balancing、provisioning；scaling, and more.<br>
目前使用container orchestration tools有以下功能:<br>
*  Allocation resources among containers(在容器中分配資源)
*  Scaling containers up and down based on workloads (根據工作附載變換容器大小)
*  Routing traffic and balancing loads(分流以及附載平衡)
*  Assigning services and applications to specific containers(給予特定容器分配服務和應用)
*  Deployment and provisioning(部屬以及配置)

1. Kubernetes
2. Gcore Managed Kubernetes
3. Gcore Container as a Service
4. Red Hat OpenShift
5. Apache Mesos
6. Amazon Elastic Container Service(Amazon ECS)
7. Google Kubernetes Engine(GKE)
8. Azure Service Fabric
9. Amazon Elastic Kubernetes Service(EKS)
10. Docker Swarm

Kubernetes(k8s)
===
K8s是Google在2008年部屬並於2014移交給Cloud Native Computing Foundation<br>
K8s是現今最廣為人知的open-source container orchestration tool, K8s帶來很多優點包含:auto-scaling and automated load balancing.<br>

![The main components of a Kubernetes cluster](https://assets.gcore.pro/blog_containerizing_prod/uploads/2023/03/top-10-container-orchestration-tools-1.png "image")
K8s的框架由4個主要conponent(元件)組成:
*  Node: 在K8s中，node負責容器附載的執行並且可以是實體也可以是虛擬的，這些machines作為容器runtimes的hosts同時也促進容器和K8s service之的通訊
*  Cluster:  Cluster是由一組nodes組成，這些nodes會share資源以及執行容器化應用程式。
*  Replication Controllers: 智慧agents用於scheduling容器之間的資源分配。
*  Labels: K8s服務所使用的tags，用於分辨容器是屬於哪一個pod。

K8s持續地在成為最受歡迎的部屬open-source平台工具，


Gcore Managed Kubernetes
===
Gcore Managed Kubernetes允許使用者較為容易的執行一個production-ready的K8s cluster，這個service幫助你從maintaining node、deployment、management、control plane management and K8s version updates中視放出來，你只需要管理工作node即可<br>
因為不需要擔心維護基礎設備，Gcore Managed K8s 允許你專心在部屬應用程式方面，這個service在全球15個地點提供服務，其中包含美國、歐洲和亞洲
![How Gcore Managed K8s works](https://assets.gcore.pro/blog_containerizing_prod/uploads/2023/03/top-10-container-orchestration-tools-2.png "image")

Gcore Managed K8s的key features如下:
*  Bare Metal worker nodel(裸機?工作節點)，除了VM之外會使用Bare Metal worker nodel來進行compute-intensivce workloads，就是運算效率的附載nodel，<font color="red">Bare Metal worker node指的是在K8s叢集中直接執行在物理伺服器上的工作節點，所謂的Bare Metal可以當作物理伺服器</font>。
*  Free cluster management with a 99.9% SLA(無須叢集管理即可達成99.9SLA)，這使Gcore Managed K8s跟Amazon EKS and GKE不同。
*  Great value prices for worker nodes(正所謂價格划算)，和Gcore Virtual Machines和Bare Metal servers相同。
*  NVIDIA GPU-based worker nodes，可用於AL/ML workloads。
*  Secure master node management(master node管理安全性)，意思是當Gcore administrators確認master node為security和stability(穩定)時沒有任何人可以change master node。
*  Autoscaling(自動調整規模)，允許你根據real-time的需求自動配置新的node以及刪除不必要的node
*  Self-healing(自我檢查)，會持續監製nodes的health以及在必要時自動recovers failed nodes。
*  Cilium CNI support(支援Cilium CNI)，除了Calico之外，該服務允許進階網路以及安全特徵來更簡單的管理large-scale K8s 部屬。

!  <font color="blue">Cilium是一個基於Extended Berkeley Packet Filter的網路解決方案，專門用於K8s這類型的叢集網路</font><br>
!  <font color="blue">Calico是K8s常見的插件之一，基於Border Gateway Protocol提供簡單且穩定的網路策略和網路隔離能力</font><br>

Gcore Container as a Service
===

Red Hat OpenShift
===

Apache Mesos
===

Amazon Elastic Container Service(Amazon ECS)
===

Google Kubernetes Engine(GKE)
===

Azure Service Fabric
===

Amazon Elastic Kubernetes Service(EKS)
===

Docker Swarm
===




>以下出自於[Google Cloud](https://cloud.google.com/learn/what-is-kubernetes?hl=zh-TW)介紹 <br>

Kubernetes(k8s)是一個以容器為中心的管理軟體，Kubernetes起源於Google Cloud並且受到Google內部叢集管理系統[Borg](https://research.google/pubs/large-scale-cluster-management-at-google-with-borg/)啟發，Kubernetes把所有部屬以及管理程式等環節都精簡畫並提供自動化的容器配置、調度等等便利功能有助於提升作業可靠性、方便性、管理性和減少運作時間和資源。

<h3>Kubernetes的定義</h3>

Kubernetes(縮寫為K8s, 8是指K~s之間有8個字母)，是一種開放原始法系統，可以在任何環境(Windows,Linux等等)部屬、擴充和管理container應用程式。<br>
k8s會自動執行容器管理的操作工作且內建多種指令用於:1)部屬應用程式、2)持續進行應用程式的變更、3)根據應用程式需求調用資源、4)監控部屬之應用程式。<br>
透過k8s的內建指令可以簡化應用程式的管理作業。<br>

<h3>Kubernetes和Docker</h3>
K8s和docker兩者雖然都是用於執行容器化應用程式的不同技術，卻能互相補足彼此的不足。<br>
Docker會讓您將執行應用程式所需要的資源全部放在一個箱子中，這個箱子可以在需要的時間和位置儲存和開啟。一但開始採用封裝應用程式的做法，就需要一種方法加以管理，<font color="blue">這就是K8s能派上用場的地方</font><br>
有幾點事情需要釐清一下:<br>
* 不論有無docker, K8s都可以使用<br>
* Docker無法取代K8s，將K8s與Docker結合，不但可以將應用程式容器化，還能大規模值行應用程式<br>
* Docker和K8s之間的差異與各自在容器化和值行應用程式中所扮演的角色有關<br>
* Docker是一種開放性業界標準，可用於將應用程式瘋裝病分散到容器中<br>
* K8s會使用Docker來部屬、管理和擴充容器化應用程式<br>

以上為Google cloud中告訴我們有關於K8s的用途以及和Docker的配合用途，接下來我們需要理解K8s的工作原理


下圖為一張K8s架構圖來自[影片](https://www.youtube.com/watch?v=RUjcGn2YeVo)
![K8s structure](image/k8s_structure.png)
圖片中包含幾個component:
*  Cluster
*  Control plane
*  node
*  pod
*  svc()
*  ing
*  deploy

1~多個container會形成pod<br>
把pod部屬到合適的node中去執行<br>
pod被視為一台虛擬的電腦主機，當執行了一個pod也代表在虛擬環境中執行了一台主機<br>
control plane會記錄這些pod的資訊並將這些pod放置到合適的node去執行<br>
也可以額外利用deploy機制來一次部屬多個pod在多個node中，control plane同樣會記錄deploy的資訊<br>

# pod網路規則
當pod都建立成功時，就需要開始處理pod間的網路連線<br>
Cluster之間有自己的內網與外部隔絕,當pod被創建時會自動給予一個隨機內網動態IP，由於這個動態IP難以掌控因此我們需要一個路由器來將外部流量導入至內部pod，這類型的路由器元件在K8s中稱為:Service。<br>
這個Service資訊也會被記錄在Control plane之中，當pod之間的網路可以互通時就需要開始建立Cluster內部與外部的網路連線。<br>
這時候需要一個虛擬路由器來進行對接，這類型的路由器我們稱為Ingress controller，在實體Cluster當中以pod的形式存在，當我們設定好ingress規則就可以由Ingress controller將流量導入至service再傳遞給對應的pod。<br>

------

此外還有一個namespace的元件用於管理pod和service，每一個pod和service都會隸屬於某個namespace，Kubernetes會為每個pod和service建立各自的DNS Record讓Cluster內部的應用程式之間可以透過這個簡單的DNS規則相互溝通。

透過以上可以大致了解目前Kubernetes中整個Cluster運作的元件以及架構，其中最重要的是control plane，control plane會記錄與管理主要元件(pod,service,ingress controller等等)資訊並且元件與元件之間的關聯與互動同樣會記錄起來




