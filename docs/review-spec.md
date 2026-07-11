# AI Infra 技术审查规范

## 审查目标
确保每篇发布内容的**技术准确性**、**数据可溯源性**和**行业中立性**，避免因事实错误在公共平台遭到专业质疑。

## 审查 Agent 职责
1. **事实核查**：所有技术参数（带宽/容量/性能数字）必须与官方白皮书或权威基准对齐
2. **来源验证**：每个数据点必须标注可追溯来源（NVIDIA/AMD/Intel 官方文档、MLPerf 榜单、Gartner/IDC 报告）
3. **红线检查**：确认无招聘话术、无过度国产捆绑（周二至周四禁国产）
4. **术语一致性**：技术术语使用规范，无歧义
5. **图文一致性**：正文描述与配图内容一致，图中的数据与正文引用的数据吻合
6. **时效性检查**：引用的数据是否为最新版本（如 MLPerf 版本号、产品代号）

## 审查清单（每篇必查）

### A. 数据准确性
- [ ] A1: 所有带宽数值（GB/s、Gbps、TB/s）与官方 spec sheet 一致
- [ ] A2: 所有容量数值（GB、TB）与官方产品页一致
- [ ] A3: 性能对比数据（如加速比）有明确来源标注
- [ ] A4: 市场规模数据标注来源（IDC/Gartner）及年份
- [ ] A5: MLPerf 数据标注具体版本号（如 v4.0）

### B. 技术术语
- [ ] B1: 芯片代号正确（Hopper/Ampere/Blackwell/CDNA3）
- [ ] B2: 互联技术名称正确（NVLink 4.0 / Infinity Fabric / CXL 3.0）
- [ ] B3: 软件栈名称正确（CUDA 12.x / ROCm 6.0 / oneAPI）
- [ ] B4: 无张冠李戴（如把 AMD 的技术归给 NVIDIA）

### C. 红线合规
- [ ] C1: 无"转岗/招聘/HC/投递简历"等话术
- [ ] C2: 周二至周四无国产算力提及
- [ ] C3: 周五国产算力为客观列举，非主角推荐
- [ ] C4: 标签包含固定三标签 + 专属标签

### D. 图文一致性
- [ ] D1: 正文引用的数据与图中展示的数据一致
- [ ] D2: 图中数据来源标注完整
- [ ] D3: 配图内容与正文主题匹配
- [ ] D4: 图序与正文"配图索引"描述一致

### E. 格式规范
- [ ] E1: 正文 ≤150 字
- [ ] E2: 配图 5-6 张
- [ ] E3: YAML front matter 完整
- [ ] E4: 末尾有话题标签

## 审查输出格式

```
## 审查报告：YYYY-MM-DD [主题]

### 审查结果：✅ 通过 / ⚠️ 需修改 / ❌ 不通过

### 详细检查

#### A. 数据准确性
- A1: ✅/❌ [说明]
- A2: ✅/❌ [说明]
...

#### B. 技术术语
...

#### C. 红线合规
...

#### D. 图文一致性
...

#### E. 格式规范
...

### 需修改项
1. [具体问题 + 修改建议]
2. ...

### 审查结论
[一段总结]
```

## 关键数据参考库（审查 Agent 使用）

### GPU 互联带宽
| 技术 | 带宽 | 来源 |
|------|------|------|
| NVLink 4.0 (H100) | 900 GB/s 双向 | NVIDIA H100 Whitepaper |
| NVLink 3.0 (A100) | 600 GB/s 双向 | NVIDIA A100 Whitepaper |
| Infinity Fabric (MI300X) | 832 GB/s | AMD MI300X Whitepaper |
| PCIe 5.0 x16 | 128 GB/s 双向 | PCIe SIG |

### HBM 规格
| 芯片 | HBM代 | 容量 | 带宽 | 来源 |
|------|-------|------|------|------|
| NVIDIA H100 SXM | HBM3 | 80 GB | 3.35 TB/s | NVIDIA H100 Whitepaper |
| AMD MI300X | HBM3 | 192 GB | 5.3 TB/s | AMD MI300X Whitepaper |
| Intel Gaudi2 | HBM2e | 96 GB | 2.45 TB/s | Intel Gaudi2 Whitepaper |
| NVIDIA B200 | HBM3e | 192 GB | 8.0 TB/s | NVIDIA Blackwell Whitepaper |

### 市场规模
| 数据点 | 值 | 来源 |
|--------|-----|------|
| 2023 AI Infra 市场 | ~$66B | IDC AI Infrastructure Spending Guide 2024 |
| 2027E AI Infra 市场 | ~$298B | IDC Forecast |
| CAGR | ~35% | IDC 计算 |

### 软件生态
| 维度 | CUDA | ROCm | oneAPI |
|------|------|------|--------|
| 深度学习算子 | cuDNN ★★★ | MIOpen ★★☆ | oneDNN ★★☆ |
| BLAS | cuBLAS ★★★ | rocBLAS ★★★ | oneMKL ★★★ |
| 多卡通信 | NCCL ★★★ | RCCL ★★☆ | - ★☆☆ |
| 推理优化 | TensorRT ★★★ | - ★☆☆ | - ★☆☆ |
| 开发者规模 | ~400万 | ~50万 | ~20万 |
