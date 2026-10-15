# MP3000 — Engineering Project with Sustainability

**Final-year capstone project (2026–27).** This repository is intentionally a project statement for now: the design work has started, but no source code has been written yet. Code, models and documentation will be added here as the project progresses.

## The project

**Real-time hand-gesture recognition driving a robotic arm** — a self-proposed topic, supervised by **Dr Yu Zhou**.

A webcam feed is classified by a lightweight neural network into a small set of hand gestures. Each recognised gesture selects a pre-taught action, which a small desktop robotic arm then replays. Object positions are fixed, so the arm behaves as a **demonstration actuator** rather than a general manipulator and no inverse kinematics is required.

## Design goals

| Goal | Approach |
|---|---|
| **Low-power edge inference** | The model is deliberately kept small and the compute budget constrained, so inference runs in real time on an embedded / edge board rather than a workstation. That trade-off — not raw accuracy — is the technical contribution. |
| **Sustainability** | Assistive control for users who cannot operate a keyboard or joystick (accessibility), longer usable device life, and **measured energy consumption per inference** as a quantitative sustainability metric. |
| **Privacy by design** | The camera observes only the author and public datasets — no third-party subjects — so no ethics approval or data-protection approval is needed. |
| **Bounded scope** | Gesture **classification** only: no hand-keypoint estimation and no end-to-end regression; replay of taught trajectories instead of motion planning. |

## Status

| Item | State |
|---|---|
| Topic proposal | Written and submitted (October 2026) |
| Supervisor | Dr Yu Zhou |
| Hardware | Small educational 4-DOF desktop robotic arm — **to be confirmed** |
| Repositories | This one (introduced now, populated as work proceeds) |

## Planned structure

```
docs/        proposal, literature notes, design decisions, test results
firmware/    embedded-side inference and actuator control
model/       dataset preparation, training scripts, quantised/exported models
pc-app/      host-side capture, labelling and demonstration tooling
```

## Notes

- The project is assessed as a technical report plus a poster defence, with a separate pass/fail non-technical report on sustainability.
- Nothing in this repository is a claim of completed work: it is the project's public statement of intent.

---

# MP3000 —— 可持续工程毕业设计

**大四毕业设计（2026–27 学年）。** 本仓库目前**有意只做项目简介**：设计工作已经开始，但还没有写任何源码。代码、模型与文档会随进度陆续补进来。

## 项目是什么

**实时手势识别驱动机械臂** —— 自拟题目，导师 **Dr Yu Zhou**。

摄像头画面经轻量神经网络分类为若干手势；识别出的手势用来选择一段预先示教好的动作，由一台小型桌面机械臂复现。由于物体位置固定，机械臂充当的是**演示执行器**而非通用操作手，因此**不需要逆运动学**。

## 设计目标

| 目标 | 做法 |
|---|---|
| **低功耗边缘实时推理** | 刻意把模型做小、把算力预算压住，让推理在嵌入式 / 边缘板卡上实时跑，而不是在工作站上跑。技术贡献在**这个取舍**，不在堆准确率。 |
| **可持续性** | 为无法使用键盘/摇杆的用户提供辅助控制（无障碍）、延长设备可用寿命，并把**每次推理的实测能耗**作为可量化的可持续性指标。 |
| **隐私优先** | 摄像头只拍本人与公开数据集，不涉及第三方受试者，因此不需要伦理审批与数据保护审批。 |
| **范围可控** | 只做手势**分类**：不做手部关键点估计、不做端到端回归；用示教轨迹复现代替运动规划。 |

## 当前状态

| 项 | 状态 |
|---|---|
| 选题表 | 已填写并提交（2026 年 10 月） |
| 导师 | Dr Yu Zhou |
| 硬件 | 小型教学用 4 自由度桌面机械臂 —— **待确认** |
| 仓库 | 即本仓库（先建，随进度填充） |

## 规划的目录结构

```
docs/       选题材料、文献笔记、设计决策、测试结果
firmware/   嵌入式端推理与执行器控制
model/      数据集准备、训练脚本、量化/导出模型
pc-app/     上位机采集、标注与演示工具
```

## 说明

- 本模块的考核方式为技术报告 + 海报答辩，另有单独一份"可持续性"非技术报告（Pass/Fail）。
- 本仓库中的任何内容都不代表工作已完成：它是这个项目的公开意向说明。

