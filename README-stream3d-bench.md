---
license: apache-2.0
language:
  - en
task_categories:
  - visual-question-answering
  - question-answering
tags:
  - vision-language-model
  - video-question-answering
  - 3d-vision
  - spatial-understanding
  - streaming-video
  - multimodal
  - benchmark
---

# 🏆 Stream3D-Bench

Stream3D-Bench is a comprehensive benchmark with **10,000 QA samples** for evaluating online 3D spatial understanding in vision-language models. It is introduced with [Stream3D-VLM: Online 3D Spatial Understanding with Incremental Geometry Priors](https://arxiv.org/abs/xxx).

<p align="center">
  <img src="https://stream3d-vlm.github.io/images/3-data_generation_v3.png" width="90%" />
</p>

Unlike conventional offline 3D understanding benchmarks that assume complete scene observations or predefined clips, Stream3D-Bench evaluates models in a streaming setting. Models must process temporally ordered visual inputs, decide when to respond, and answer spatial questions that require observation, memory, or future monitoring.

<p align="center">
  <img src="https://stream3d-vlm.github.io/images/s2-benchmark_distribution_v2.png" width="90%" />
</p>

## 🌟 Features

- 10,000 QA samples for online 3D spatial understanding in streaming video
- Covers **5 cognitive competencies**, **3 temporal interaction modes**, and **29 subtasks**
- Includes numerical, multiple-choice, and open-ended answer formats
- Evaluates response accuracy, response timing, and inference latency
- Built from diverse RGB-D video sources including ScanNet, ScanNet++, and ARKitScenes
- Designed for both proprietary and open-source vision-language model evaluation

## 🧠 Task Taxonomy

Stream3D-Bench spans **5 cognitive competencies**:

- Ego-Motion Estimation
- Environment Measurement
- Object-Camera Relationship
- Object Attributes
- Object Chronology

It is organized into **3 temporal interaction modes**:

- **Forward Response (Monitoring)**: tasks that require monitoring future events and responding at the right time
- **Realtime Perception (Observation)**: tasks that require understanding the current frame and immediate surroundings
- **Backward Tracing (Memory)**: tasks that require recalling and reasoning about past observations from the video stream

Together, these settings form **29 subtasks** covering diverse spatio-temporal 3D perception and reasoning scenarios.

## 📊 Evaluation

Stream3D-Bench evaluates online 3D vision-language models under a **1 fps streaming video setting**. The benchmark measures both answer quality and online interaction behavior, including whether a model responds at the correct time.

Answer types include:

- **NA**: numerical answers
- **MCA**: multiple-choice answers
- **OEA**: open-ended answers

## 🚀 Usage

Please refer to the official repository for:

- Benchmark data format
- Evaluation scripts
- Model inference examples
- Metric definitions
- Visualization examples

Repository: https://github.com/hanxunyu/Stream3D-VLM

## 📝 Citation

If you find Stream3D-Bench useful for your research or applications, please consider citing our work:

```bibtex
@article{yu2026stream3d,
  title={Stream3D-VLM: Online 3D Spatial Understanding with Incremental Geometry Priors},
  author={Hanxun Yu and Xuan Qu and Lei Ke and Boqiang Zhang and Yuxin Wang and Jianke Zhu and Dong Yu},
  journal={arXiv preprint arXiv:xxxx.xxxxx},
  year={2026}
}
```
