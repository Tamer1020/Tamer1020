# Tamer Areij

**Junior Computer Vision / AI Engineer · Perception · Robotics Software · Edge AI**

I work on mobile robot navigation and computer vision in Python and C++. My projects include a ROS 2 robot that changes viewpoint to inspect a gauge, a road damage detector and a camera health monitor.

Based in Germany. Available for **full-time junior engineering roles** and open to relocation to **Dubai, Abu Dhabi and the wider UAE**.

## Featured Engineering Projects

### 01 · [InspectLoop](https://github.com/Tamer1020/InspectLoop) — Autonomous Gauge Inspection

A mobile robot navigates a simulated warehouse with ROS 2 and Nav2, then uses OpenCV to read analog pressure gauges. When a pipe hid part of gauge PG-12, the robot moved twice before accepting a reading of **6.7833 bar**. A second gauge stayed unreadable and was logged as **unresolved**.

**[Watch the mission · 1 min 37 s](https://github.com/Tamer1020/InspectLoop/releases/download/v3.2.0/InspectLoop-Demo-V2.mp4)** · [PG-12 reinspection · 34 s](https://github.com/Tamer1020/InspectLoop/releases/download/v3.2.0/InspectLoop-PG12-V2.mp4) · [Recorded mission report](https://github.com/Tamer1020/InspectLoop/blob/main/docs/media/capture/20261115_140724_e358/mission_report.md)

[![InspectLoop in Gazebo beside the onboard camera’s rectified view of gauge PG-12.](https://raw.githubusercontent.com/Tamer1020/InspectLoop/main/docs/media/v2/InspectLoop-V2-Cover.jpg)](https://github.com/Tamer1020/InspectLoop/releases/download/v3.2.0/InspectLoop-Demo-V2.mp4)

**Next step · Deep learning for gauge reading.** I plan to train a PyTorch model to locate six landmarks on the dial and compare it with the current ArUco/OpenCV reader on held-out gauge panels. I’ll measure pressure error, how often each reader returns a reading, and how often it accepts an incorrect one when the dial is partly hidden or viewed at an angle.

---

### 02 · Road Damage Detection

**From road images to an inspectable inference service.** A YOLOv8n pipeline for four road-damage classes: validated RDD2022 data preparation, training and evaluation, FastAPI image inference, ONNX export verification and CPU benchmarking.

**Stack:** Python · PyTorch · OpenCV · ONNX Runtime · FastAPI · Docker

**[Repository](https://github.com/Tamer1020/road-damage-detection) · [60-second demo](https://github.com/Tamer1020/road-damage-detection/blob/main/assets/demo/road-damage-demo.mp4) · [Model card & evidence](https://github.com/Tamer1020/road-damage-detection/blob/main/docs/MODEL_CARD.md) · [Error analysis](https://github.com/Tamer1020/road-damage-detection/blob/main/docs/ERROR_ANALYSIS.md)**

[![Road Damage Detection demo: an input road image beside the actual annotated API response](https://raw.githubusercontent.com/Tamer1020/road-damage-detection/main/assets/demo/poster.jpg)](https://github.com/Tamer1020/road-damage-detection/blob/main/assets/demo/road-damage-demo.mp4)

*Demo replays real HTTP responses from the released model, including successful detections and failure cases. Chapter timing is edited.*

- **Historical validation:** **24.5% mAP@50** and **34.0% recall** on 565 RDD2022 Czech validation images.
- **Historical CPU benchmark:** **21.466 ms mean latency**, **2.76× lower than PyTorch CPU**, on an Intel i7-13650HX. Ten images, 100 timed calls; image decoding excluded.
- **Current engineering checks:** **62 unit/contract tests**, plus real-weight PyTorch/ONNX verification and HTTP smoke checks in [CI](https://github.com/Tamer1020/road-damage-detection/actions/workflows/ci.yml).

Export agreement checks backend consistency, not detection accuracy. Independent route/country validation and embedded-device performance remain unmeasured.

---

### 03 · Road Camera Health Monitor

**Camera-quality diagnostics for perception pipelines.** An OpenCV / NumPy pipeline for recorded video that uses per-camera calibration and temporal persistence to detect degradation and emit fault events, annotated video and CSV/JSON reports. No trained model or GPU is required.

**Stack:** Python · OpenCV · NumPy · pytest · GitHub Actions

**[Repository](https://github.com/Tamer1020/road-camera-health-monitor) · [60-second demo](https://github.com/Tamer1020/road-camera-health-monitor/blob/main/docs/demo/road-camera-health-demo.mp4) · [Evaluation & scope](https://github.com/Tamer1020/road-camera-health-monitor/blob/main/docs/EVALUATION.md) · [Engineering design](https://github.com/Tamer1020/road-camera-health-monitor/blob/main/docs/DESIGN.md)**

[![Road Camera Health Monitor demo: the same synthetic startup-blur clip with a healthy file baseline and an automatic baseline](https://raw.githubusercontent.com/Tamer1020/road-camera-health-monitor/main/docs/demo/poster.jpg)](https://github.com/Tamer1020/road-camera-health-monitor/blob/main/docs/demo/road-camera-health-demo.mp4)

*Actual pipeline output on a synthetic scene with injected faults. The demo shows how the calibration reference changes a startup-blur decision.*

- **Reported synthetic detection:** **100% steady-state recall** on each target fault clip, after the fault ramp and temporal hold-down, using a known-healthy file baseline.
- **Reported clean-clip behavior:** **0 false-alarm events** on one **16-second synthetic clip**.
- **Historical container benchmark:** **57.6 source frames/s — 2.31× realtime**, including annotated-video output, at 640×360 with 25 fps input.

The evaluation uses 11 clips from one generated scene, with thresholds selected on that corpus. These results do not establish field accuracy or target edge-device throughput; real-camera validation remains future work.

## Experience & Education

**Computer Vision & AI Internship · Performise Labs · 2026**

Automotive perception prototypes: object detection, drivable-area and lane segmentation, nuScenes camera experiments, PyTorch training/evaluation, knowledge distillation, quantization, ONNX export and model benchmarking. Internship code is not public.

**B.Sc. Electrical Engineering and Information Technology · TU Dortmund University, Germany**

All B.Sc. degree requirements completed. Available for full-time Junior Computer Vision, Perception and Edge AI roles.

**Academic mobile robotics · C++ / ROS**

Sequential homing and Pure Pursuit waypoint tracking, with odometry, TF coordinate transforms, velocity control, RViz visualization and transform/timing debugging.

## Technical Skills

| Area | Tools and practice |
|---|---|
| Computer vision & ML | PyTorch, OpenCV, NumPy, YOLOv8 / YOLO-OBB, object detection, segmentation, knowledge distillation |
| Inference & evaluation | ONNX / ONNX Runtime, FastAPI, mAP evaluation, latency/FPS benchmarking, post-training quantization |
| Software & robotics | Python, C++, Linux, Git, Docker, pytest, GitHub Actions, ROS, ROS 2, Nav2, TF, RViz |

## Contact

**[LinkedIn — Tamer Areij](https://www.linkedin.com/in/tamer-areij-881216176/)**

Germany · Available for full-time junior roles · Open to UAE relocation
