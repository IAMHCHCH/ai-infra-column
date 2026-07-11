## 审查报告：2026-07-15 HBM3 内存带宽瓶颈

### 审查结果：⚠️ 需修改

### 详细检查

#### A. 数据准确性
- A1: ✅ HBM3 带宽 5.3TB/s（MI300X）— 与参考库一致（AMD MI300X Whitepaper）
- A1: ✅ 配图 img4_comparison.svg 中三卡带宽数据正确：H100 = 3.35TB/s, MI300X = 5.3TB/s, Gaudi2 = 2.45TB/s
- A2: ✅ MI300X 192GB / H100 80GB — 与参考库一致
- A2: ✅ 配图 img4_comparison.svg 中三卡容量数据正确：H100 = 80GB, MI300X = 192GB, Gaudi2 = 96GB
- A3: ✅ "MI300X 凭 192GB 单卡跑 70B" — 70B 模型推理需约 140GB FP16 内存，192GB 充裕，逻辑正确
- A4: ✅ 无市场规模数据
- A5: ✅ 无 MLPerf 数据

#### B. 技术术语
- B1: ✅ MI300X 代号正确（CDNA3 架构，已通过 AMD 官方页面验证）
- B2: ✅ HBM3 术语正确（H100 和 MI300X 均使用 HBM3）
- B3: ✅ 无软件栈相关内容
- B4: ✅ 无张冠李戴

#### C. 红线合规
- C1: ✅ 无招聘/转岗/HC 话术
- C2: ✅ 周三内容，无国产算力提及
- C3: ✅ 无国产算力内容
- C4: ✅ 标签包含固定三标签 + #HBM3 #AMDMI300X

#### D. 图文一致性
- D1: ✅ 正文 "5.3TB/s" 与封面 SVG (img1_cover.svg) 及配图 img4_comparison.svg 中的 5.3 TB/s 一致
- D1: ✅ 正文 "192GB" 与配图中 192 GB 一致
- D1: ✅ 正文 "H100 仅 80GB" 与配图中 80 GB 一致
- D2: ✅ img4_comparison.svg 标注 "Data Source: NVIDIA / AMD / Intel Official Spec Sheets"
- D3: ✅ 配图内容（HBM 架构、三卡对比）与正文 HBM3 主题匹配
- D4: ✅ 封面 SVG 展示了 HBM3 Stack 架构和带宽对比，与正文主题一致

#### E. 格式规范
- E1: ✅ 正文约 75 字（含标点），≤150 字
- E2: ✅ 配图 5 张，符合 5-6 张要求
- E3: ❌ **缺少 YAML front matter**（无 date/topic/tags 字段）
- E4: ✅ 末尾有话题标签

### 需修改项
1. **❌ 缺少 YAML front matter**：正文开头缺少 `---date/topic/tags---` 字段，需补充：
   ```yaml
   ---
   date: 2026-07-15
   topic: HBM3 内存带宽瓶颈
   tags: #AIInfra #GPU编程 #高性能计算 #HBM3 #AMDMI300X
   ---
   ```
2. **缺少配图索引**：正文未列出配图索引说明，建议补充
3. **Gaudi2 HBM 类型标注**：配图 img4_comparison.svg 中 Gaudi2 标注为 "HBM2e" ✅ 正确（参考库一致）
4. **封面 SVG 中标注 "12-Hi"**：MI300X 使用 12-Hi HBM3 堆叠，此为正确规格，✅ 无误
5. **配图 SVG 中 "MI300X: 2.4× 容量 + 1.6× 带宽 vs H100"**：192/80 = 2.4× ✅，5.3/3.35 = 1.58× ≈ 1.6× ✅，计算正确

### 审查结论
所有 HBM 带宽和容量数据均与官方白皮书一致。三卡对比图数据准确，加速比计算正确。主要问题是缺少 YAML front matter 和配图索引。技术内容质量优秀。
