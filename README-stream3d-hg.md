---
license: apache-2.0
language:
- en
metrics:
- accuracy
base_model:
- Qwen/Qwen2.5-VL-3B-Instruct
library_name: transformers
tags:
- vision-language-model
- 3d-vision
- multimodal
- spatial-understanding
- streaming-video
pipeline_tag: image-text-to-text
---

<p align="center">
  <img src="https://stream3d-vlm.github.io/images/logo.png" width="160" />
</p>
<h2 align="center">
Stream3D-VLM: Online 3D Spatial Understanding<br>with Incremental Geometry Priors
</h2>

<h4 align="center">
  <b>Project Page:</b> <a href="https://stream3d-vlm.github.io/">stream3d-vlm.github.io</a> | 
  <b>GitHub:</b> <a href="https://github.com/hanxunyu/Stream3D-VLM">hanxunyu/Stream3D-VLM</a>
  <br><br>
  <a href="https://stream3d-vlm.github.io/"><img src="https://img.shields.io/badge/Project-Home Page-green?logo=safari&logoColor=white" alt="Project Home Page"></a>
  <a href="https://github.com/hanxunyu/Stream3D-VLM"><img src="https://img.shields.io/badge/GitHub-Repository-blue?logo=github" alt="GitHub Badge"></a>
  <a href="https://huggingface.co/datasets/JonnyYu828/Stream3D-1M-Dataset"><img src="https://img.shields.io/badge/HuggingFace-Dataset-orange?logo=huggingface" alt="Hugging Face Dataset"></a>
  <a href="https://huggingface.co/datasets/JonnyYu828/Stream3D-Bench"><img src="https://img.shields.io/badge/HuggingFace-Benchmark-blueviolet?logo=huggingface" alt="Hugging Face Benchmark"></a>
  <a href="https://arxiv.org/abs/xxxx"><img src="https://img.shields.io/badge/arXiv-xxxxx-b31b1b.svg?logo=arxiv&logoColor=red" alt="arXiv"></a>
</h4>


---

## 📰 News

* **2026.05** — Released [Stream3D-Bench](https://huggingface.co/datasets/JonnyYu828/Stream3D-Bench).
* **2026.05** — Released [Stream3D-1M-Dataset](https://huggingface.co/datasets/JonnyYu828/Stream3D-1M-Dataset).
* **2026.05** — Released [Stream3D-VLM-4B](https://huggingface.co/JonnyYu828/Stream3D-VLM-4B).

---

## 🌟 Model Overview

**Stream3D-VLM** is an online 3D vision-language model that supports **real-time spatial understanding and interaction directly from streaming video**. Unlike existing 3D Large Multimodal Models that operate in offline settings and require complete scene observations or predefined video clips, Stream3D-VLM enables efficient and continuous 3D scene comprehension without offline processing.

To address the scarcity of streaming 3D–language data, we develop a scalable data generation pipeline that curates **over 1M online spatio-temporal 3D QA pairs** ([Stream3D-1M](https://huggingface.co/datasets/JonnyYu828/Stream3D-1M-Dataset)) and establish a comprehensive benchmark with **10,000 QA samples**, spanning **29 subtasks** across **5 cognitive competencies** and **3 temporal interaction modes** ([Stream3D-Bench](https://huggingface.co/datasets/JonnyYu828/Stream3D-Bench)).

<p align="center">
  <img src="https://stream3d-vlm.github.io/images/pipeline.png" width="90%" />
</p>

---

## 🧠 Key Characteristics

- **Online 3D Spatial Understanding**: Real-time spatial reasoning from streaming video without requiring full scene reconstruction upfront.

- **Incremental Geometry Priors**: The VSFI module injects temporally aligned geometric features from a 3D reconstruction model into the visual stream as video unfolds.

- **Streaming Control Modeling**: Learns *when* to respond or remain silent via joint optimization of streaming control loss and standard language modeling loss.

- **Efficient Long-Context Inference**: The plug-and-play GAVC module dynamically compresses visual tokens guided by 3D structure, reducing decoding overhead for real-time deployment.

- **Comprehensive Benchmark**: Stream3D-Bench covers Forward Response (monitoring), Realtime Perception (observation), and Backward Tracing (memory) across diverse spatio-temporal 3D tasks.

---

## 🚀 Main Results

### Stream3D-Bench (Online Evaluation)

Stream3D-VLM consistently outperforms competing proprietary and open-source models on [Stream3D-Bench](https://huggingface.co/datasets/JonnyYu828/Stream3D-Bench), delivering the most accurate response timing and the lowest inference latency. Results are reported under a **1 fps** streaming video setting. NA / MCA / OEA denote numerical, multiple-choice, and open-ended answers, respectively.

<p align="center">
  <img src="https://stream3d-vlm.github.io/images/table_2_Stream3DBench_result.png" width="95%" />
</p>

> **Bold** and <u>underlined</u> values indicate the best and second-best results, respectively. More details can be found on our [paper](https://arxiv.org/abs/xxxx).

### VSI-Bench (Offline Evaluation)

Despite being designed for streaming scenarios, Stream3D-VLM also performs well across all subtasks of the offline spatial perception and reasoning benchmark, significantly surpassing both commercial and open-source models.

<p align="center">
  <img src="https://stream3d-vlm.github.io/images/table_3_VSIBench_result.png" width="95%" />
</p>

---

## 📦 Related Resources

| Resource | Link |
| -------- | ---- |
| Training Dataset | [JonnyYu828/Stream3D-1M-Dataset](https://huggingface.co/datasets/JonnyYu828/Stream3D-1M-Dataset) |
| Benchmark | [JonnyYu828/Stream3D-Bench](https://huggingface.co/datasets/JonnyYu828/Stream3D-Bench) |
| Code | [hanxunyu/Stream3D-VLM](https://github.com/hanxunyu/Stream3D-VLM) |
| Project Page | [stream3d-vlm.github.io](https://stream3d-vlm.github.io/) |

---

## Citation

If you find Stream3D-VLM useful for your research or applications, please consider citing our work using the following BibTeX:

```bibtex
@article{yu2026stream3d,
    title={Stream3D-VLM: Online 3D Spatial Understanding with Incremental Geometry Priors},
    author={Hanxun Yu and Xuan Qu and Lei Ke and Boqiang Zhang and Yuxin Wang and Jianke Zhu and Dong Yu},
    journal={arXiv preprint arXiv:xxxx.xxxxx},
    year={2026}
}
```
