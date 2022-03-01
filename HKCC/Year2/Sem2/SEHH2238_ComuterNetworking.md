# SEHH2238 Computer Networking
  
  
## Tabel of Content
- [Ch1 Data Communication](https://github.com/JackTheCoconut/Notebook/blob/main/HKCC/Year2/Sem2/SEHH2238_ComuterNetworking.md#ch1-data-communication)
- [Ch2 ]
- [Ch3 ]
  
  
## Ch1 Data Communication
    
>Data Communications 係指兩部 devices 之間交換data 
    
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
  >Networking 係指由 coummunication channels 連埋 ge 一 set nodes (又名 devices)
 
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

### vi. Protocols
