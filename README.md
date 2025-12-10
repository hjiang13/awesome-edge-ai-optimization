
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


## 📊 4. Benchmarks and Datasets
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
