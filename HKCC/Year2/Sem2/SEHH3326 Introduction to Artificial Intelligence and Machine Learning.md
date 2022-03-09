# SEHH3326 Introduction to Artificial Intelligence and Machine Learning
>喱一科真係好有趣 :D , 不過睇真 D 原來係 Discrete Math >:(  

![meme](https://media.discordapp.net/attachments/684958583367925771/950704047038533652/1ndk5RDalDDjnCp0QFFhiWg.png)


## Table of Content
- [Ch1 Introduction to AI and ML](#ch1-introduction-to-ai-and-ml)
- [Ch2 Searching]
- [Ch3 Adversarial Search]
- [Ch4 Logical Agents and Reasoning]

--------------------------------------------------------------------------------------------------------------------------------------
## Ch1 Introduction to AI and ML
>咩係 AI 同 ML?

### i. Artificial Intelligence (AI)  
>對於 AI 一詞，唔同學者都有唔同 ge expectation  
>Psychologist:[Human Peformance/Thought/Process] vs Engineer:[Rationality/Behaviour/Result]  
>psychologist (心理學家)認為 AI 應該要 behaves like a human (**Human performance**)  
>Computer Engineer 認為 AI 應該要可以 efficiently, quickly, cheaply 咁 achieve the goal (do the right things) (**rationality 理性**)  
>但係大多數 ge AI researcher 都係注重係 result 多個 process  
  
<img src="https://i.imgflip.com/67v1zt.jpg" width=40% height=50%>

- Intelligence
  - 指識得 Learning (學習), Reasoning (推理), Understanding (理解) environment ge 野

- Artificial Intelligence (AI)
  - 指一個可以 show 到 Intelligence 特性 ge 一個由人所 build ge entities 

- Computer programming vs AI
  - 係 computer ge 世界入面，你要知道點樣去 solve 嗰 problem，再 step by step (programming) 咁教電腦  
  - 係 AI ge 世界，你唔洗知點樣去 solve 嗰 problem 而係話比 AI 知你想要 D 咩  

- AI vs ML
 - AI 係用 reasoning, thinking 同 logics 去 solve problems
 - ML 係用大量 example 去 solve, 同埋識進化 (improve)  
 
- Turning Test
  - 一個攞喱 check AI 夠唔夠 human ge test，但係其實都幾難 pass 到  

### ii. History of AI
> 諗到 AI 喱一樣 ge 人真係好 big brain
> 早期 ge AI 因為 computing power ge 不足，一直都受到限制

- Expert systems  
  >早期類似 AI 概念 ge 一個 system
  - 由一大堆 if then statment 所組成
  - 唔識進化
  - 理解唔到新野
  - 好難 maintain

- Late 1980's
  - Probabilistic reasoning (probability + statistic)
  - Machine learning

- Early 2000's
  - Big Data

- Early 2010's
  - Deep Learning 

### iii. Application of AI

### iv. Limitation of AI
> 盡管 AI 睇好似似萬能咁，但係其實 AI 都有唔擅長 ge 野
> 語言博大精深
- E.g. Language translation, story telling 
- The rule of language often contradict itself
- A single word can have various meaning 
- New word being created constantly  

### v. Intelligent Agents
> 一個 agent 係由 Architecture 同 agent program 所組成
> 為左可以整到一個 Rational agent，我地需要一 D performance measur，一個 environment，再加上兩類 architecures
- Performance measure
- Environment
- Actuators (執行)
- Sensors  
  
*而當中 Environments 入面又有分唔同 types*  
>為左方便去認，以下會以 player 代指 agent  

- Fully vs Partially observable
  - 就**環境**而言，我地係咪知道哂所有資訊?  
  
- Single-agent vs Multiagent
  - 得一個 player? 定係仲有其他player?
  - 雙方可以係 competitive or cooperative ge 關係  

- Deterministic vs Nondeterministic 
  - 當 player 做出一個動作嗰時，會唔會知道嗰結果?  

- Episodic vs Sequential
  - player 所做 ge 每一個 move 係獨立 ge? 定係因影響之後 ge move?  

- Discrete vs Continuous
  - 周圍 ge 環境，時間，規則同動作係一格一格咁跳，定係連續咁喐動?  
  - Jason 講到一個例子：如果嗰 environment 係用電子鐘 ge 話，咁就係discrete，但係如果係用秒針一直喐 ge 嗰隻鐘(唔係一秒一秒跳嗰 D)就係 continuous  

- Static vs Dynamic vs Semidynamic
  - Static 指，環境會等到 player 做出一個動作之後先會改變
  - Dynamic 指，環境係會係 player 諗緊嗰時都可以做出改變 (例如對手做左一個動作都計改變左嗰環境)
  - Semidynamic 指，環境雖然唔係會 player 做出動作之前改變，但 player ge performance score 卻可以  

- Known vs Unknown
  - 哩一項並唔關嗰 environment 事，而係關 player 本身
  - Known enviroment 係指 player 知道會一個動作 ge outcome (or probability outcomes) 係咩
  - Unknow environment 就係 player 知佢可以做咩，但唔知嗰 enviroment 會點變

*除左關於 environment 之外，仲有關於 agent programs*
> agent program 可以話係 Brain of agent
> 最常見 ge 有以下四種  
  
- Simple reflex agents
  > 一種淨係會 focus 係當下環境而作出決定 ge agents
  - 靠 if then rules 去做決定  
  <img src="https://media.discordapp.net/attachments/684958583367925771/951021882923175956/unknown.png" width=50% height=50%>  

- Model-based reflex agents
  > 一種會 base on 當下 ge environment 同過住經驗去做決定 ge agents  
  - agent 會保持住一種叫 internal state ge state
  - internal state 係由 Transition model 同 Sensor model 去作 update
    - Transition model 會話比 agent 知嗰環境係點變 (may or may not depend of agent's actions)
    - Sensor model 會話比 agent 知嗰環境會點樣影響嗰知覺 
    
- Goal-based agents
  -  
<img src="https://media.discordapp.net/attachments/684958583367925771/951025320620863498/unknown.png" width=50% height=50%>  

- Utility-based agents  
  - 
<img src="https://media.discordapp.net/attachments/684958583367925771/951025429525979156/unknown.png" width=50% height=50%>  
