# 下周 AI Infra 内容拆分计划表

> **周期**：2026-07-13（周一）至 2026-07-18（周六）
> **模块归属**：第一部分「AI Infra 认知篇」+ 第二部分「AI Infra 技术栈篇」启动
> **目标**：完成专栏首发周，建立读者对 AI Infra 全栈认知框架

---

## 📅 周一 7/13 — 周知识地图

**主题**：AI Infra 到底是什么？本周知识地图

**内容方向**：
- 定义 AI Infra 的边界（硬件+网络+存储+软件栈）
- 范式转移：CPU 通用计算 → GPU 并行计算 → 超异构（GPU+NPU+DPU）
- 本周4个微知识点预告拆解

**配图重点**：
- 图1封面："AI Infra 全景地图"
- 图2：AI Infra 四层架构全景图（硬件/网络/存储/软件）
- 图3：从 CPU 到 GPU 到超异构的范式演进时间线
- 图4：Gartner/IDC 对 AI 基础设施市场规模预测
- 图5：NVIDIA DGX SuperPOD — 当今最强 AI 集群一览

**标签**：#AIInfra #GPU编程 #高性能计算 #AInfra入门

---

## 📅 周二 7/14 — 深度微专题①

**主题**：NVIDIA NVLink 4.0 的拓扑演进

**内容方向**：
- NVLink-C2C 提供 900 GB/s 双向带宽，是 PCIe 5.0 的 7 倍
- NVSwitch 全互联拓扑：从 DGX A100 的 6-switc 到 DGX H100 的 4-switch
- 为什么多卡训练瓶颈不在算力而在互联

**厂商案例**：
- NVIDIA H100 NVLink 拓扑（官方白皮书数据）
- Meta Grand Teton 平台的 NVLink 布线实践

**配图重点**：
- 图4：H100 vs MI300X 互联带宽对比（数据来源：NVIDIA/AMD 官方 spec sheet）
- 图5：Meta Grand Teton 集群 NVSwitch 拓扑实拍

**标签**：#AIInfra #GPU编程 #高性能计算 #NVDIAH100 #NVLink

---

## 📅 周三 7/15 — 深度微专题②

**主题**：HBM3 内存——为什么大模型推理卡在显存带宽

**内容方向**：
- HBM3 vs HBM3e：带宽从 3.35 TB/s 到 4.8 TB/s 的跃迁
- 为什么 LLM 推理是 memory-bandwidth bound（roofline 模型分析）
- NVIDIA H100 (80GB HBM3) vs AMD MI300X (192GB HBM3) vs Intel Gaudi2 (96GB HBM2e)

**厂商案例**：
- NVIDIA H100 HBM3 架构白皮书
- AMD MI300X 大容量 HBM3 在 LLM 推理中的优势
- SK Hynix/Samsung HBM3e 路线图

**配图重点**：
- 图4：三款加速器 HBM 容量/带宽对比柱状图（数据来源：各厂商 spec）
- 图5：AMD MI300X 192GB HBM3 如何支撑 70B 模型单卡推理

**标签**：#AIInfra #GPU编程 #高性能计算 #HBM3 #AMDMI300X

---

## 📅 周四 7/16 — 深度微专题③

**主题**：CUDA 护城河——为什么 NVIDIA 软件生态难以撼动

**内容方向**：
- CUDA 生态全景：cuDNN / cuBLAS / NCCL / TensorRT
- ROCm 和 oneAPI 的追赶策略与差距
- PyTorch 2.0 + Triton 如何降低 CUDA 绑定度

**厂商案例**：
- NVIDIA CUDA 12.x 新特性（如 fp8 支持）
- AMD ROCm 6.0 对 PyTorch 的原生支持进展
- Intel oneAPI + SYCL 在 Gaudi 加速器上的实践

**配图重点**：
- 图4：CUDA vs ROCm vs oneAPI 生态成熟度对比（功能覆盖率矩阵）
- 图5：PyTorch 2.0 编译流程：torch.compile → Triton kernel 生成

**标签**：#AIInfra #GPU编程 #高性能计算 #CUDA #ROCm

---

## 📅 周五 7/17 — 行业多样性观察（唯一国产窗口）

**主题**：从 NVIDIA 到多元算力：AI 芯片的百花齐放

**内容方向**：
- 后摩尔定律时代，单一架构无法满足所有场景
- 全球 AI 芯片格局：NVIDIA / AMD / Intel / Google TPU / AWS Trainium
- 国内算力生态客观简介：鲲鹏（通用 CPU）、昇腾（AI NPU）、飞腾等在特定场景的落地
- 核心调性：技术多样性视角，不吹不黑，客观数据说话

**配图重点**：
- 图4：全球 AI 芯片性能/能效象限图（含国内外厂商，数据来源：MLPerf / 公开论文）
- 图5：AI 芯片多样性生态地图（按场景分类：训练/推理/边缘）

**标签**：#AIInfra #GPU编程 #高性能计算 #AI芯片 #算力多样性

---

## 📅 周六 7/18 — 互动/资料汇总

**主题**：AI Infra 第一周核心术语表 & 入门论文推荐

**内容方向**：
- 本周术语表：NVLink / NVSwitch / HBM3 / CUDA / ROCm / oneAPI / Roofline 模型
- 推荐论文/文档：NVIDIA Hopper Whitepaper、AMD MI300X Whitepaper、MLPerf Inference v4.0 Results
- 互动：你最想深入了解 AI Infra 的哪个方向？

**配图重点**：
- 图1封面："AI Infra 术语速查表"
- 图2-5：术语卡片图（每个术语一句话解释+图示）

**标签**：#AIInfra #GPU编程 #高性能计算 #论文推荐

---

## ✅ 验收检查清单

- [ ] 周二至周四案例全部为 NVIDIA/AMD/Intel，无国产生态内容
- [ ] 周五内容为"行业多样性观察"，国产算力作为客观列举非主角
- [ ] 全文无"转岗/招聘/HC/投递"等敏感词
- [ ] 每篇正文 ≤150 字
- [ ] 每篇配图 5-6 张，数据图表标注来源
- [ ] 标签包含固定三标签 + 专属标签
