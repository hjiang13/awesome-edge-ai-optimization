
# Awesome Edge Computing Optimization & Autonomous Driving Papers
A curated and continuously updated list of research papers on **edge computing**,  
**performance optimization**, **autonomous driving systems**, and **AI on small devices**  
(e.g., ESP32, microcontrollers, embedded systems).

Maintained by: Hailong Jiang (Youngstown State University)

---

## 1. Edge Computing Systems & Optimization

### 1.1 Surveys / Overall Optimization

- **S. Dong et al.** “Task Offloading Strategies for Mobile Edge Computing: A Survey.” *Computer Networks*, 2024.  
  `[survey][offloading][MEC]` :contentReference[oaicite:0]{index=0}  

- **Y. Qin et al.** “Task offloading optimization in mobile edge computing based on deep reinforcement learning.” *Scientific Reports*, 2025.  
  `[DRL][task offloading][latency]` :contentReference[oaicite:1]{index=1}  

- **Y. Zheng.** “Survey of Distributed Task Offloading Optimization Based on Heuristic Algorithms in Edge Computing.” *Academic Journal of Science and Technology*, 2025.  
  `[survey][heuristics][meta-heuristic]` :contentReference[oaicite:2]{index=2}  

- **J. Pournazari et al.** “Computation Offloading in the Edge-to-Cloud Continuum: A Survey.” *Cluster Computing*, 2025.  
  `[survey][edge–cloud continuum]` :contentReference[oaicite:3]{index=3}  

- **Z. Mohammed et al.** “Optimization in Edge Computing: A Survey.” *IJSeR*, 2023.  
  `[survey][optimization models]` :contentReference[oaicite:4]{index=4}  

- **S. Dong et al.** “A Survey on Computation Offloading with Task Types.” *arXiv*, 2024.  
  `[survey][task types][MEC]` :contentReference[oaicite:5]{index=5}  

### 1.2 Classic Edge Inference / Co-Execution

- **Y. Kang et al.** “Neurosurgeon: Collaborative Intelligence Between the Cloud and Mobile Edge.” *ASPLOS*, 2017.  
  `[DNN partition][cloud–edge co-inference]` :contentReference[oaicite:6]{index=6}  

- **N. Lane et al.** “DeepX: A Software Accelerator for Low-Power Deep Learning Inference on Mobile Devices.” *IPSN*, 2016.  
  `[software accelerator][layer compression][mobile]` :contentReference[oaicite:7]{index=7}  

- **L. Huynh et al.** “DeepMon: Mobile GPU-based Deep Learning Framework for Continuous Vision.” *MobiSys*, 2017.  
  `[GPU offload][mobile vision][framework]` :contentReference[oaicite:8]{index=8}  

- **A. Mathur et al.** “DeepEye: Resource Efficient Local Execution of Multiple Deep Vision Pipelines on Mobile Devices.” *MobiSys*, 2017.  
  `[multi-pipeline][local execution][optimization]` :contentReference[oaicite:9]{index=9}  

- **A. Bhattacharya et al.** “DeepCache: Principled Cache for Mobile Deep Vision.” *MobiCom*, 2018.  
  `[cache][temporal redundancy][latency reduction]` :contentReference[oaicite:10]{index=10}  

### 1.3 DRL / Scheduling / Resource Management

- **Y. Sun et al.** “Vehicular task offloading and job scheduling method based on cloud–edge computing.” *IEEE T-ITS*, 2023.  
  `[vehicular edge][scheduling][cloud–edge]` :contentReference[oaicite:11]{index=11}  

- **Recent works** on heterogeneous resource management & dynamic task offloading in MEC (e.g., dynamic resource scheduling, DRL-based scheduling) 可以参考最新的 MEC 资源调度综述。:contentReference[oaicite:12]{index=12}  

> 你可以在 README 里写一句：  
> *For more MEC offloading / scheduling works, see also the reference lists in the surveys above.*

---

## 2. Autonomous Driving & Edge AI

### 2.1 Cooperative / Collaborative Perception & V2X

- **Y. Ji et al.** “Toward Autonomous Vehicles: A Survey on Cooperative Perception.” *IEEE Access*, 2024.  
  `[survey][cooperative perception][V2X]` :contentReference[oaicite:13]{index=13}  

- **Y. Wang et al.** “V2X Cooperative Perception for Autonomous Driving: Recent Advances and Challenges.” *arXiv*, 2023.  
  `[survey][V2X][CP frameworks]` :contentReference[oaicite:14]{index=14}  

- **Q. Liu et al.** “AdaMap: High-Scalable Real-Time Cooperative Perception at the Edge.” *IEEE/ACM SEC*, 2023.  
  `[CP system][edge server][latency guarantees]` :contentReference[oaicite:15]{index=15}  

- **R. Yu et al.** “Edge-Assisted Collaborative Perception in Autonomous Driving.” *IEEE/ACM SEC Workshop*, 2021.  
  `[architecture][edge RSU assistance][scheduling]` :contentReference[oaicite:16]{index=16}  

- **F. Hawlader et al.** “Cooperative Perception Using V2X Communications: An Experimental Study.” *2024*.  
  `[experimental][V2X CP][real-time]` :contentReference[oaicite:17]{index=17}  

- **A. Sarlak et al.** “Extended Visibility of Autonomous Vehicles via Optimized Cooperative Perception.” *Transportation Research Part C*, 2025.  
  `[optimization][CP][perception range]` :contentReference[oaicite:18]{index=18}  

- **Collaborative Perception Datasets Repo.** “Collaborative-Perception-Datasets-for-Autonomous-Driving.” GitHub, 2025.  
  `[datasets][CP][benchmark collection]` :contentReference[oaicite:19]{index=19}  

### 2.2 Automotive Edge Computing & Mapping

- **Q. Liu et al.** “EdgeMap: CrowdSourcing High Definition Map in Automotive Edge Computing.” *IEEE ICC*, 2022.  
  `[HD map][edge][crowdsourcing]` :contentReference[oaicite:20]{index=20}  

- **Q. Liu et al.** “Real-Time Dynamic Map with Crowdsourcing Vehicles in Edge Computing.” *IEEE T-IV*, 2022.  
  `[dynamic HD map][edge computation]` :contentReference[oaicite:21]{index=21}  

- **Y. Zhang et al.** “CrowdSourcing Live High-Definition Map via Collaborative Computation in Automotive Edge Computing.” *IEEE T-VT*, 2024.  
  `[live HD map][collaborative edge]` :contentReference[oaicite:22]{index=22}  

- **Q. Liu et al.** “CAVE: Crowdsourcing Passing-By Vehicles for Reliable In-Vehicle Edge Computing.” *IEEE GLOBECOM*, 2024.  
  `[vehicular edge][reliability][crowdsourcing]` :contentReference[oaicite:23]{index=23}  

- **Q. Liu et al.** “AdaMap: High-Scalable Real-Time Cooperative Perception at the Edge.” (同上，这里既属于 CP 也属于 automotive edge system) :contentReference[oaicite:24]{index=24}  

> 这一类里，你可以专门开一节 “Automotive Edge Computing (Mapping & CAV Systems)” 来放 HD map / CAV-edge 的论文。

---

## 3. TinyML & AI on Microcontrollers (含 ESP32 / MCU 方向)

### 3.1 TinyML / On-Device Inference Surveys

- **S. Heydari et al.** “Tiny Machine Learning and On-Device Inference: A Survey.” *Sensors*, 2025.  
  `[survey][TinyML][latency vs cloud]` :contentReference[oaicite:25]{index=25}  

- **S. Somvanshi et al.** “From Tiny Machine Learning to Tiny Deep Learning: A Survey.” *ACM Computing Surveys*, 2025.  
  `[survey][TinyDL][hardware/software stack]` :contentReference[oaicite:26]{index=26}  

- **A Comprehensive Survey on TinyML.** 2023.  
  `[survey][taxonomy][applications]` :contentReference[oaicite:27]{index=27}  

- **N. Alajlan et al.** “TinyML: Enabling of Inference Deep Learning Models on Microcontrollers.” *Electronics*, 2022.  
  `[MCU][DL inference][resource constraints]` :contentReference[oaicite:28]{index=28}  

- **R. Immonen et al.** “Tiny Machine Learning for Resource-Constrained Devices.” 2022.  
  `[TinyML][soft sensors][sensor fusion]` :contentReference[oaicite:29]{index=29}  

- **Y. A. Soliman et al.** “A Comprehensive Systematic Review of TinyML for Person Detection.” *IJCS*, 2021.  
  `[application][person detection][TinyML]` :contentReference[oaicite:30]{index=30}  

- **J. D. Velasquez et al.** “Emerging Trends and Strategic Opportunities in Tiny Machine Learning.” *Neurocomputing*, 2025.  
  `[survey][trends][opportunities]` :contentReference[oaicite:31]{index=31}  

### 3.2 Frameworks / Practical Deployment

- **Embedded.com Tutorial.** “Deploying Neural Networks on Microcontrollers with TinyML.” 2025.  
  `[tutorial][deployment][MCU]` :contentReference[oaicite:32]{index=32}  

- TensorFlow Lite Micro, Edge Impulse, Arduino-Pico / ESP32-TinyML 项目可以放在 *Tools & Frameworks* 小节，用列表列出。

> 关于 **ESP32 专门的论文**，可以放在一个子类 “ESP32 Case Studies”，目前可以先从应用型 TinyML/MCU 论文开始，后续你可以按关键词 “ESP32 TinyML detection / classification / energy” 慢慢往里加。

---

## 4. Cross-Layer Optimization  
（Compiler-Level, MLIR, LLM for Code Optimization —— 这里放你的 IR/MLIR/LLM4IR 相关灵感）

### 4.1 Surveys / Overviews

- **Z. Wang, M. F. P. O’Boyle.** “Machine Learning in Compiler Optimisation.” *Proceedings of the IEEE*, 2018.  
  `[survey][ML for compiler][loop/phase ordering]` :contentReference[oaicite:33]{index=33}  

- **A. Haj-Ali.** “Machine Learning in Compiler Optimization.” *UC Berkeley EECS Technical Report EECS-2021-2*, 2021.  
  `[dissertation][ML4Comp][optimization problems]` :contentReference[oaicite:34]{index=34}  

- **H. Zhang et al.** “Compiler Technologies in Deep Learning Co-Design: A Survey.” *Intelligent Computing*, 2023.  
  `[survey][DL compiler][co-design]` :contentReference[oaicite:35]{index=35}  

- **J. Gong et al.** “Language Models for Code Optimization.” *arXiv*, 2025.  
  `[survey][LLMs][code optimization]` :contentReference[oaicite:36]{index=36}  

- **A. Haj-Ali et al.** (multiple works summarized in the Berkeley TR 上) – AutoPhase, NeuroVectorizer, etc. 可以在 README 中作为一组 “ML-guided optimization passes” 的代表。:contentReference[oaicite:37]{index=37}  

### 4.2 MLIR / IR-Level Infrastructure

- **MLIR Project (LLVM).** “Multi-Level Intermediate Representation (MLIR).”  
  `[infrastructure][multi-level IR][heterogeneous]` :contentReference[oaicite:38]{index=38}  

- **R. Golin et al.** “Towards a High-Performance AI Compiler with Upstream MLIR.” *arXiv*, 2024.  
  `[MLIR-based AI compiler][performance]` :contentReference[oaicite:39]{index=39}  

- **Buddy Compiler / buddy-mlir.** 系列工作：Buddy Compiler 项目 + “Compiler Technologies in Deep Learning Co-Design” 等。  
  `[MLIR dialects][tensor compiler][agent-like pass pipelines]` :contentReference[oaicite:40]{index=40}  

- **awesome-mlir.** “A curated list of useful resources for MLIR.” GitHub.  
  `[resource list][papers+talks]` :contentReference[oaicite:41]{index=41}  

### 4.3 LLM & ML for Compiler / Systems Optimization

- **GitHub Repo.** “awesome-machine-learning-in-compilers.”  
  `[curated list][ML4Comp][datasets+papers]` :contentReference[oaicite:42]{index=42}  

- **DeCOS: Data-Efficient Reinforcement Learning for Compiler Optimization.** *ICS 2025*.  
  `[RL for compiler passes][data-efficient]` :contentReference[oaicite:43]{index=43}  

- 多篇关于 MLGO、CompilerGym 等项目的论文，可以作为 “ML for Pass Scheduling / Flag Tuning” 的子列表，相关资源在 awesome-machine-learning-in-compilers 里有比较系统的整理。:contentReference[oaicite:44]{index=44}  

> 对你自己的 LLM4IR / vectorization 研究，可以在这一节单独加一个小 subsection：  
> **4.4 Jiang Group (IR-Aware LLM / Vectorization / Edge AI)**  
> 写上 “in preparation / work-in-progress” 的 ideas 和 preprint 链接，以后有 arXiv 就可以直接挂上去。



---

## 🤝 Contributing
Pull requests welcome!  
If you want to add a paper, please include:
- Title
- Year / Venue
- Link
- 2–3 sentence summary

---

## ⭐ Star History
(You can add a star-history badge later)

---

## 📄 License
MIT License
