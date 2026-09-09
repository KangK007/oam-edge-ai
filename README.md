# oam-edge-ai

> OAM 端侧 AI —— 从云端训练到边缘设备推理的全链路工程实践

## 背景 (Background)

端侧 AI（On-Device / Edge AI）正在成为 AI 落地的主流形态：低延迟、离线可用、隐私安全、带宽成本可控。
本项目的目标是完整走通一条 **「PyTorch 训练 → ONNX 导出 → C++ 推理 → 边缘设备部署」** 的真实技术链路，
而不是只停留在 "跑过某个模型" 的层面。

## 目标 (Goals)

- 训练一个可在端侧运行的轻量级模型（PyTorch）
- 完成 ONNX 模型导出与精度校验
- 使用 C++（ONNX Runtime）编写端侧推理代码
- 在边缘设备上落地并输出 benchmark 数据
- 形成一套可复用的端侧 AI 工程模板

## 技术路线 (Roadmap)

```
PyTorch (训练) → ONNX (模型转换) → C++ / ONNX Runtime (推理) → Edge Device (部署)
```

| 阶段 | 技术选型 | 状态 |
| ---- | -------- | ---- |
| 数据准备 | Python / dataset 目录 | 📋 规划中 |
| 模型训练 | PyTorch | 📋 规划中 |
| 模型转换 | ONNX / onnxruntime | 📋 规划中 |
| 端侧推理 | C++ / ONNX Runtime / CMake | 📋 规划中 |
| 性能测试 | benchmark 目录 | 📋 规划中 |

## 目录结构 (Structure)

```
oam-edge-ai/
├── dataset/         # 数据集：原始数据与预处理脚本
├── train/           # 训练代码：PyTorch 模型定义、训练与验证
├── models/          # 训练产出的权重文件
├── onnx/            # ONNX 导出脚本与转换后的模型
├── cpp_inference/   # C++ 端侧推理代码（CMake 工程）
├── benchmark/       # 端侧性能测试（延迟 / 内存 / 功耗）
└── docs/            # 设计文档、踩坑记录、参考资料
```

## 当前状态 (Status)

- [x] 项目骨架 V0.1：仓库目录结构初始化
- [ ] 数据集准备与预处理
- [ ] PyTorch 模型训练
- [ ] ONNX 模型导出
- [ ] C++ 端侧推理
- [ ] 边缘设备部署与 benchmark

Version: **V0.1** (骨架阶段) · License: MIT
