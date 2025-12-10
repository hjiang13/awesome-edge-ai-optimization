
# Awesome Edge Computing Optimization & Autonomous Driving Papers
A curated and continuously updated list of research papers on **edge computing**,  
**performance optimization**, **autonomous driving systems**, and **AI on small devices**  
(e.g., ESP32, microcontrollers, embedded systems).

Maintained by: Hailong Jiang, Ph.D. (hjiang@ysu.edu Youngstown State University)

---

## 🔥 1. Edge Computing Optimization
Papers focused on system-level or algorithmic optimization:

### ✔️ Edge Offloading & Scheduling
- Paper Title (Year) — Summary…
- Paper Title (Year) — Summary…

### ✔️ GPU / CPU Co-optimization
- Paper Title (Year) — Summary…

### ✔️ SIMD / Vectorization for Edge AI
- Paper Title (Year) — Summary…

---

## 🚗 2. Autonomous Driving + Edge AI
Papers involving perception, V2X, and vehicle–edge cooperation:

### ✔️ Cooperative Perception
- Paper Title (Year) — Summary…

### ✔️ On-vehicle Optimization
- Paper Title (Year) — Summary…

### ✔️ Lightweight Models for Auto-Driving
- Paper Title (Year) — Summary…

---

## 📡 3. Embedded AI / ESP32 / TinyML
AI models designed for extremely constrained devices.

## **MCUNet: Tiny Deep Learning on IoT Devices**  
**Ji Lin, Wei-Ming Chen, Yujun Lin, John Cohn, Chuang Gan, Song Han, NeurIPS 2020**  
🔗 https://proceedings.neurips.cc/paper/2020/hash/380d9c86004355ea4e6bf37c062b1f5a-Abstract.html  

### **Summary:**  
This paper presents **MCUNet**, an end-to-end TinyML framework that jointly designs:  

1. **TinyNAS** — a resource-aware neural architecture search method that tailors the search space based on constraints such as SRAM, Flash, latency, or energy.  
2. **TinyEngine** — an extremely lightweight inference engine optimized for microcontrollers, featuring global memory scheduling instead of layer-wise allocation.

Together, TinyNAS + TinyEngine reduce SRAM usage by **3.4×**, outperform TF-Lite Micro and CMSIS-NN by **1.7–3.3×**, and achieve **>70% ImageNet top-1 accuracy** on commercial MCUs using **3.5× less SRAM** and **5.7× less Flash** compared to quantized MobileNetV2 or ResNet-18.

The paper demonstrates that *ImageNet-scale inference is achievable on tiny microcontrollers*, pushing TinyML capabilities forward.

### **Tags:**  
[TinyML] [MCUNet] [NAS] [TinyEngine] [Memory Scheduling] [Microcontroller Inference]  


---

## **TinyML: Analysis of Xtensa LX6 Microprocessor for Neural Network Applications by ESP32 SoC**  
**Md Ziaul Haque Zim, arXiv 2021**  
🔗 https://arxiv.org/abs/2106.10652  
DOI: https://doi.org/10.48550/arXiv.2106.10652

### **Summary:**  
This paper analyzes the computational ability of the **Xtensa LX6 dual-core processor** inside the ESP32 SoC for TinyML tasks. It benchmarks the feed-forward latency of neural networks with varying input sizes and hidden-layer configurations, showing how model complexity influences inference speed.

The results indicate that ESP32—often considered a low-power IoT microcontroller—can in fact perform lightweight neural network inference. With support from MicroPython and TensorFlow Lite Micro, ESP32 becomes a practical, low-cost platform for deploying TinyML applications.

### **Tags:**  
[TinyML] [ESP32] [Xtensa LX6] [microcontroller inference] [embedded neural networks]  

---
## **MicroNets: Neural Network Architectures for Deploying TinyML Applications on Commodity Microcontrollers**  
**Colby Banbury, Chuteng Zhou, Igor Fedorov, Ramon Matas, Urmish Thakker, Dibakar Gope, Vijay Janapa Reddi, Matthew Mattina, Paul Whatmough, MLSys 2021**  
🔗 https://proceedings.mlsys.org/paper/2021/hash/7ef605fc8dba5425d6965fbd4c8fbe1f-Abstract.html  

### **Summary:**  
This paper introduces **MicroNets**, a family of neural network architectures specifically optimized for deployment on **commodity MCUs** with strict constraints on latency, memory, and energy. The key insight driving the work is an observed linear relationship between **operation (op) count** and **latency** on microcontrollers. This enables the authors to treat op count as an efficient, hardware-agnostic proxy for latency in neural architecture search.

Using this observation, the authors employ **Differentiable NAS (DNAS)** to search for architectures with minimal op count and low memory usage. The resulting MicroNet models are deployed using TensorFlow Lite Micro and demonstrate **state-of-the-art performance** on the three TinyMLPerf benchmark tasks:  

- Visual wake words  
- Audio keyword spotting  
- Anomaly detection  

All models and training scripts are available at: https://github.com/ARM-software/ML-zoo.

### **Tags:**  
[TinyML] [MicroNets] [NAS] [DNAS] [MCU Inference] [TinyMLPerf] [Resource-Constrained ML]

## **Machine Learning for Microcontroller-Class Hardware: A Review**  
**Swapnil Sayan Saha, Sandeep Singh Sandha, Mani Srivastava, IEEE (Review Paper)**  
🔗 https://ieeexplore.ieee.org/document/xxxxx  *(use your actual link)*  

### **Summary:**  
This comprehensive survey reviews the full stack of technologies required to enable **machine learning on microcontroller-class hardware**—devices with extremely limited compute, memory, and energy budgets. The paper outlines how conventional ML workflows must be re-engineered when targeting ultraresource-constrained IoT nodes.

The authors propose a **closed-loop TinyML development workflow** that includes:  
- Data engineering tailored to low-end devices  
- Feature projection and compact representation  
- Pruning, quantization, and encoding for efficiency  
- Deployment workflows that respect strict compute & latency constraints  

The survey highlights several representative TinyML applications (image recognition, anomaly detection, speech, control tasks, mHealth, visual wake words) and provides both qualitative and numerical insights into model development across these scenarios.

The paper concludes with a set of **open research challenges**, such as optimal model compression, energy-aware NAS, cross-platform TinyML benchmarking, and addressing the gap between algorithmic advances and hardware capabilities.

### **Tags:**  
[TinyML] [Survey] [Microcontrollers] [Resource-Constrained ML] [Model Compression] [Pruning] [Quantization] [IoT ML Workflow]

## **vMCU: Coordinated Memory Management and Kernel Optimization for DNN Inference on MCUs**  
**Size Zheng, Renze Chen, Meng Li, Zihao Ye, Luis Ceze, Yun Liang, MLSys 2024**  
🔗 https://proceedings.mlsys.org/paper/2024/hash/xxxxx  *(use actual link)*  

### **Summary:**  
This paper introduces **vMCU**, a coordinated memory management and kernel-level optimization framework designed to overcome the extreme memory limitations of microcontrollers (MCUs) when running deep neural networks. Unlike prior approaches that treat kernel execution and memory management separately, vMCU virtualizes MCU memory into a unified pool and divides it into **kernel-specific segments**. These segments can be loaded, stored, and overlapped dynamically during DNN execution.

The key insight is that **fine-grained segment-level memory control** enables overlapping lifetimes of tensors, eliminating the need to materialize all intermediate tensors simultaneously. As a result, vMCU effectively reduces the memory footprint of DNN inference.

Experiments on ARM Cortex-M4 and Cortex-M7 processors show:  
- **12.0% → 49.5% reduction in RAM usage**  
- **20.6% → 53.0% reduction in energy consumption**  
compared to state-of-the-art MCU inference baselines.

Overall, vMCU reduces memory bottlenecks by **up to 61.5%**, enabling deployment of larger and more sophisticated neural networks on low-end MCUs.

### **Tags:**  
[TinyML] [MCU Memory Management] [Kernel Optimization] [vMCU] [Low-end MCU Inference] [Memory Virtualization]

## **Accelerating TinyML Inference on Microcontrollers Through Approximate Kernels**  
**Giorgos Armeniakos, Georgios Mentzos, Dimitrios Soudris, ICECS 2024 (IEEE)**  
🔗 https://ieeexplore.ieee.org/document/10848979  
DOI: 10.1109/ICECS61496.2024.10848979  

### **Summary:**  
This paper explores the use of **approximate computing** combined with **kernel design optimization** to accelerate CNN inference on microcontrollers (MCUs), where strict limits on RAM and Flash pose major challenges for TinyML deployment.

The authors propose a **kernel-based approximation framework** that:  
1. **Unpacks convolution operands** and computes their significance offline.  
2. Uses this significance to drive a **computation-skipping strategy**, selectively omitting low-impact operations.  
3. Explores a design space to identify **Pareto-optimal trade-offs** between accuracy and latency.

Evaluations on an STM32-Nucleo MCU with CNNs trained on CIFAR-10 show:  
- **≈21% latency reduction** with *no degradation* in Top-1 accuracy (for high-accuracy settings).  
- Even larger reductions when slight accuracy loss is acceptable.

The results demonstrate that **approximated kernels can substantially accelerate inference on resource-constrained MCUs**, especially when task tolerates minor precision trade-offs.

### **Tags:**  
[TinyML] [Approximate Computing] [Approximate Kernels] [MCU Inference] [Latency Optimization] [Edge AI]

## **Can LLMs Revolutionize the Design of Explainable and Efficient TinyML Models?**  
**Christophe El Zeinaty, Wassim Hamidouche, Glenn Herrou, Daniel Menard, Merouane Debbah, arXiv 2025**  
🔗 https://arxiv.org/abs/2504.09685  
DOI: https://doi.org/10.48550/arXiv.2504.09685  

### **Summary:**  
This paper proposes a novel framework for designing **efficient, interpretable TinyML neural architectures** using large language models (LLMs) as the core engine for neural architecture search (NAS). The method integrates three components:  

1. **LLM-guided hierarchical NAS** balancing accuracy, computation (MACs), and memory usage.  
2. **Vision Transformer (ViT)–based knowledge distillation** to enhance generalization without increasing model size.  
3. **An explainability module** that helps derive interpretable architecture decisions.

Using Pareto optimization and KD, the authors refine architectures under strict MCU constraints. On CIFAR-100, the three proposed TinyML-tailored models (LMaNet-Elite, LMaNet-Core, QwNet-Core) achieve:  
- **74.50%**, **74.20%**, and **73.00%** accuracy  
- All within **<100M MACs**  
- Satisfying the **320 KB SRAM budget** of STM32H7 microcontrollers  

These results surpass strong SOTA TinyML baselines such as **MCUNet-in3/in4** and **XNNpack-derived models**, highlighting the potential of combining **LLM-driven NAS + KD + explainability** for generating deployable and efficient MCU models.

### **Tags:**  
[TinyML] [LLM-guided NAS] [Explainability] [Knowledge Distillation] [Model Compression] [MCU Deployment] [Efficient Architecture Search]


## 4. Kernel Generation

## **Reinforcement Tuning Open Source LLMs for Kernel Generation**  
**Aksh Garg, Jeffrey Heo, Megan Mou, Stanford University**  
🔗 *(add arXiv/URL if available)*  

### **Summary:**  
This paper investigates reinforcement learning (RL)–based post-training methods to enhance open-source LLMs’ ability to generate **correct and efficient CUDA kernels**. The authors first apply supervised fine-tuning (SFT) on rollouts from GPT-4.1 to densify reward signals for code generation tasks. They then introduce **Group Relative Policy Optimization (GRPO)** with a composite reward function that includes:

- **Compilability**  
- **Functional correctness**  
- **Relative runtime speed**

Using the **KernelBench** benchmark, the tuned LLaMA-8B model achieves:  
- **25% correctness (up from 0%)**  
- **Avg runtime within 2.5× of native PyTorch kernels**  
- Closing **one-third of the gap** to GPT-4.1 CUDA kernel quality  

The authors also propose an **LLM-as-a-judge mechanism** to densify sparse rewards, demonstrating that such reward engineering is critical for bootstrapping functional kernel generation in low-resource open-source models. The approach provides a practical recipe for improving code generation where baseline RL methods typically fail due to sparse or zero rewards.

### **Tags:**  
[LLM4Code] [Kernel Generation] [RLHF] [GRPO] [CUDA] [LLM-as-a-Judge] [Compiler Optimization] [Open-Source Models]

## 📊 5. Benchmarks and Datasets
- OpenPilot dataset…
- CARLA benchmark…
- Edge server logs datasets…

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
