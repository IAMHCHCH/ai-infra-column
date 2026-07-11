## 审查报告：2026-07-18 术语表+论文推荐

### 审查结果：⚠️ 需修改

### 详细检查

#### A. 数据准确性
- A1: ✅ 术语卡片 img2_terms.svg 中 NVLink 4.0 = 900GB/s — 与 NVIDIA 官方一致
- A1: ✅ 术语卡片中 HBM3 数据：H100 = 80GB/3.35TB/s, MI300X = 192GB/5.3TB/s — 与参考库一致
- A2: ✅ 容量数据正确
- A3: ✅ 无性能对比数据
- A4: ✅ 无市场规模数据
- A5: ✅ 术语卡片中 MLPerf Inference v4.0 — 版本号正确

#### B. 技术术语
- B1: ✅ 术语名称正确：NVLink、NVSwitch、HBM3、CUDA、ROCm、oneAPI、RoCE、InfiniBand、TCO、Agent Infra
- B2: ✅ 互联技术名称正确（NVLink/NVSwitch/RoCE/InfiniBand）
- B3: ✅ 软件栈名称正确（CUDA/ROCm/oneAPI）
- B4: ✅ 无张冠李戴
- B5: ✅ 术语卡片中 NVSwitch 描述正确："DGX H100 使用 4 个 L2 NVSwitch 连接 8 卡" — DGX H100 确实使用 4 个 L2 NVSwitch

#### C. 红线合规
- C1: ✅ 无招聘/转岗/HC 话术
- C2: ✅ 周六内容，国产算力规则不适用
- C3: ✅ 无国产算力内容
- C4: ✅ 标签包含固定三标签 + #论文推荐

#### D. 图文一致性
- D1: ✅ 正文提到 "NVLink/HBM3/CUDA/ROCm/IB 等 10 个核心术语" — 配图 img2_terms.svg 中展示了 NVLink、NVSwitch、HBM3、CUDA 4 个术语（标注 1/4），与正文描述一致
- D2: ✅ img2_terms.svg 底部标注 "数据来源：NVIDIA/AMD/Intel 官方白皮书 · MLPerf 基准榜单"
- D3: ✅ 配图内容（术语卡片+论文推荐）与正文主题匹配
- D4: ⚠️ 正文配图索引写 "图2-5：术语卡片"，但实际仅有 img2_terms 一张图（4 个术语卡片在同一张 SVG 中），与索引描述"图2-5"不一致

#### E. 格式规范
- E1: ✅ 正文约 95 字（含标点），≤150 字
- E2: ❌ **配图仅 2 张**（img1_cover + img2_terms），不满足 5-6 张要求
- E3: ✅ YAML front matter 完整（date/topic/tags 均有）
- E4: ✅ 末尾有话题标签

### 需修改项
1. **❌ 配图数量不足**：仅有 2 张配图（封面+术语卡片），远少于 5-6 张要求。建议将术语卡片拆分为 4 张独立图片（NVLink/NVSwitch/HBM3/CUDA 各一张），或增加更多术语卡片图（ROCm/oneAPI/RoCE/InfiniBand 等），使总数达到 5-6 张
2. **配图索引与实际图片不匹配**：正文写 "图2-5：术语卡片（NVLink/NVSwitch/HBM3/CUDA/ROCm/oneAPI/RoCE/InfiniBand/TCO/Agent Infra）" 暗示有 4 张术语图，但实际只有 1 张 img2_terms.svg。需要要么拆分为多张图，要么修改配图索引描述
3. **论文推荐数量**：正文写 "附 3 篇必读论文"，img2_terms.svg 中也展示了 3 篇论文（Hopper Whitepaper / MI300X Whitepaper / MLPerf Inference v4.0），✅ 一致
4. **论文标题准确性**：img2_terms.svg 中 "[3] MLPerf Inference v4.0" — 建议补充完整论文标题和作者/机构信息

### 审查结论
术语数据准确，与参考库完全一致。论文推荐数量与正文描述匹配。主要问题是配图数量严重不足（仅2张 vs 要求5-6张），需要拆分术语卡片或增加更多图片。建议补充配图后通过。
