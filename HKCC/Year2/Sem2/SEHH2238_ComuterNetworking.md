# SEHH2238 Computer Networking
  
  
## Tabel of Content
- [Ch1 Data Communication](#ch1-data-communication)
- [Ch2 ]
- [Ch3 ]
  
----------------
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
>*n = total number of nodes (devices)*


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
![Ring](https://media.discordapp.net/attachments/684958583367925771/948875827351785472/unknown.png)  
     - adv:
       - 易安裝，易重裝
     - dis:
       - total ge devices 數受限
       - 因為 **Unidirectional traffic** (單向傳輸) ge 特性，一部 devices down 左，成候 Ring 就死左  
       
  5. Hybrid Topology  
*Hybrid Topology 係指由唔同 Topology 組成 ge Topology，無咩特別*  
  
### vi. Protocols  
>Protocols 可以理解成 a set of rules ，大家都要follow喱一 set rule 去制定佢地 ge services   
>確保大家可以 work together     
哩一 set rules 由三大組織所設立:  
- ISO  -- International Standards Orgagnization
- ANSI -- American Natinoal Standards Institute
- IEEE -- Institute of Electrical and Electronics Engineers  

**Layering**  
>每層 Layer 都係 a package of protocals
>每層 Layer 都會有自己 ge service
>但係佢地 rely on 上一層所 provide ge service 去工作

**OSI Model**  
> OSI Model 係由 ISO 係1984年所定立，由7層 Layer 所組成  
[**感謝大大無私奉獻!**](bilibili.com/video/BV1qJ411J7Tt/)  

|       |             |
|:-----:|:-----------:|
|Layer 7| Application | 
|Layer 6| Presentation|
|Layer 5| Session     |
|Layer 4| Transport   |
|Layer 3| Netwrok     |
|Layer 2| Data Link   |
|Layer 1| Physical    |
  
- Application Layer  
  > 我地要靠喱層 layer 去 access network resources
  - 喱一層 Layer 包含平時我地用開 ge application 入面所用到 ge protocol (注意唔係講緊 application 本身)
  - 用chrome去上網就係 HTTPs, HTTP
  - Gmail 就係 SMTP, POP3, IMAP 
  - upload/download 就 FTP 
  
    
- Presentation Layer
  > translate -> compress -> encrypt
  - 喱層 Layer 係將我地睇得明 ge 文字 translate 做電腦 ge 文字 
  - translate 完做電腦文字之後就會 compress 再 encrypt
  - e.g SSL for 加密同解密  
  

- Session Layer (會話層)
  > 幫你同其他電腦 or server 建立/管理/關閉一個會話
  - 喱層 Layer 會做 Authentication, Authorization 同 session management 喱幾個動作
  - Authentication 係驗証你 ge 身份
  - Authorization 係授權你 access resources 
  - Session management 係幫你 keep tracking 同管理唔同 data packets 去 ge location 

- Transport Layer
  -  
  
- Networking Layer
  -

- Data Link Layer
  -

- Physical Layer  
  -
  
  

---------------------
## Ch2 Basic Communication Principles
>
