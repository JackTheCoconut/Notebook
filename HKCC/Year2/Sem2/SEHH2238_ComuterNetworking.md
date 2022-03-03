# SEHH2238 Computer Networking
  
  
## Tabel of Content
- [Ch1 Data Communication](#ch1-data-communication)
- [Ch2 ]
- [Ch3 ]
  
  
## Ch1 Data Communication
    
>Data Communications 係指兩部 devices 之間交換data 
  
  1. [Commnication effectiveness](#i-communication-effectiveness-通訊效率)
  2. [Networking](#ii-networking)
  3. [Type of connection](#iii-type-of-connections)
  4. [Transmission mode](#iv-transmission-mode)
  5. [Topology](#v-topology)
  6. [Protocols](#vi-protocols)

    
### i. Communication effectiveness (通訊效率)    
  >Communication effectiveness(通訊效率) 係基於以下四個範疇作為評定
  1. Delivery (輸送)
      - Data 能否成功傳送到指定 ge Receiver 到
  2. Accuracy (準確率)
      - Data 送到 Receiver 到嗰時係唔係原全一致
  3. Timeliness (及時性)
      - 係唔係 Real-time transmission 
  4. Jitter (抖動)
      - signal 係傳輸 ge 過程有機會有時間上 ge 誤差，有機會造成 lag 機
      - More Info.: [Network Jitter - Common Causes and Best Solutions](https://www.ir.com/guides/what-is-network-jitter)


### ii. Networking 
  >Networking 係指由 coummunication channels 連埋 ge 一 set **nodes** (又名 **devices**)
 
  一個 Network ge quality 係由佢 ge **Performance**, **Reliability** 同 **Security** 去定
  
  1. Performance (表現)
      - Response time (響應時間)
      - Transmit time (傳輸時間)
      - Evaluted by [Networking Metrics](https://www.perfsonar.net/resources_metrics.html) 
      - e.g.: Throughput(流通量), Delay(延遲)
  2. Reliability (穩定性)
      - Frequency of failure (故障率)
      - Recovery time after a failure
          - Catastrophe(天災)
      - Resistant to:
          - Unauthorized access
          - Data damage (傳輸過程中 ge Data loss)
          - [Viruses](https://www.websecurity.digicert.com/zh/hk/security-topics/what-are-malware-viruses-spyware-and-cookies-and-what-differentiates-them)
  3. Security  (安全性)
      
  而一個 Network 又可以分為 **Local Area Networks (LANs)**, **Metropolitan Area Networks (MANs)** 同 **Wide Area Networks (WANs)**
  
  1. LANs:
      - 一個範圍入面 ge nodes 連落同一個 Network ge 叫 LAN (e.g. 一個細 office 入面 ge devices)
  2. MANs:
      - 可以認為同 LANs ge 定義差唔多，但係範圍比 LANs 大 (e.g. 一個 Town or 一個 Country)
  3. WANs:
      - 範圍上升到 World wide 咁大 

[LANs 同 MANs ge 分別?](https://www.geeksforgeeks.org/difference-between-lan-and-man/)  
   
### iii. Type of Connections
  >最主要有 **Point-to-point** 同 **Mulitpoint** 兩種

1. Point-to-point:
    
    ![Point-to-point](https://cdn.discordapp.com/attachments/684958583367925771/948295753762238505/unknown.png "Point-to-point")

2. Multipoint:
    
    ![Multipoint](https://cdn.discordapp.com/attachments/684958583367925771/948296856243437648/unknown.png "Multipoint")


### iv. Transmission Mode
  >三種唔同 ge Data flow 模式

  1. Simplex (單一)
      - 淨係得單一 data 流向 e.g. keyboard
  2. Half-duplex (半雙向)
      - 雖然係雙向，但每一次 data 淨係可以由一個 node 傳去第二個
  3. Full-duplex (全雙向)
      - 兩個 nodes 可以同時傳輪同接收 data  

### v. Topology
  >Topology 係指 nodes 之間唔同 ge 連接方法，而 nodes 之間 ge relationship 又分為 **Peer-to-peer(p2p)** or **Primary-secondary**
  >以下所有 nodes = devices
  
|                        |  Mesh  | Ring | Bus | Star |
|:----------------------:|:------:|:----:|:---:|:----:|
| Total No. of Cables    |n(n-1)/2|   n  |n + 1|   n  |
|No. of Ports per device |  n - 1 |   2  |  1  |   1  |



  1. Mesh Topology  
  *Mesh Topology 係最簡單粗暴 ge 一種做法，將所有 ge nodes 連埋一齊，咁當有一部 device down 左，  
  其他 devices 都仲可以正常咁 send and receive message.*  
  ![Mesh](https://cdn.discordapp.com/attachments/684958583367925771/948852650252841010/unknown.png)    
     - adv:
        - 唔會有 traffic problem
        - 一部機 down 左唔會影響到其他
        - Privacy 同 security 有保障
        - Easy fault identification and isolation(容易知道邊部機出左問題並加以處理)  
        - 對 p2p transmission 嚟講 
      - dis:
        - 好貴 ($$$)
        - 要求 device ge port 有一定 ge 數量以上  
      
  2. Star Topology  
*Star Topology 係近代常用 ge 一種 Network 連接方法*  
*每一部 devices 都係直接連繫到 **central controller** ，而佢地之間係唔會有 direct traffic (直接連繫)*  
![Star](https://media.discordapp.net/attachments/684958583367925771/948866270504312832/unknown.png)  
     - adv: 
       - Robustness (穩健性) //當有一個 nodes down 左都唔會影響到其他 nodes 
       - 相比起 Mesh topology 平D ($$$)
     - dis:
       - Single point of failure //如果嗰 central controller 死左，咁就GG囉  
       
  3. Bus Topology
*Bus Topology 係以一條 Long cable 作為 backbone 去 connect all devices*  
*Message 以 broadcast ge 形式去散播*  
*無咩人用lu*
![Bus](https://cdn.discordapp.com/attachments/684958583367925771/948868641154293760/unknown.png)
     - adv:
       - 易安裝
     - dis:
       - 可以裝 ge nodes 數比較少
       - Difficult reconfiguration and fault isolation (出事嗰時比較難搵邊部機出事)
      
  4. Ring Topology  
*Ring Topology 係將 D devices 連到成個圈咁，D singal 係單方向咁係 devices 同 devices 之間傳輸 (靠 repeater)*  

  5. Hybrid Topology
  
### vi. Protocols
-------------------------------------
