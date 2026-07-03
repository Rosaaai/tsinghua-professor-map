# 清华系高潜创业者 Source Map

> VC Hunter / Source 内部工具 — 一站 source 到清华系教授、合作博士生、原始 paper PDF。

## 项目简介

本工具面向 VC 从业者，整理清华大学 10 个院系、**50+ 位核心教授**、**60+ 位合作博士生** 与 **60+ 家关联创业公司**。所有论文 PDF 直链 arXiv / IEEE / Nature 系官方源，**点击即达原文**。

### 包含内容

- **第 1 部分 · 教授索引**：按院系、研究方向、"已创业 / 学术为主" 分类
- **第 2 部分 · 教授详情**：联系方式、研究代表作、研究方向（共一学生 PDF 链接）
- **第 3 部分 · 博士生名单**：跨院系汇总，每位学生挂原始 paper PDF

### 可视化

- **赛道网络图**：9 大前沿赛道 → 10 个院系 → 50+ 教授 → 60+ 公司的 4 层径向结构图
- **方向热度 Top 12**：横向柱图
- **院系创业密度**：深蓝=已创业 / 天蓝=学术

## 配色

单色蓝深浅梯度（校徽深蓝 → 冰蓝 6 阶），按节点层级切换深浅，避免色相过杂。

## 启动

这是一个纯静态站点（HTML + CSS + JS + ECharts），无后端、无构建步骤。

### 方式 1 · Python 启动本地服务器

```bash
cd tsinghua-mapper
python3 -m http.server 8099
# 浏览器打开
open http://localhost:8099/tsinghua-mapper.html
```

### 方式 2 · 直接双击打开

直接用浏览器打开 `tsinghua-mapper.html` 即可（charts 部分也能正常渲染）。

## 目录结构

```
tsinghua-mapper/
├── tsinghua-mapper.html      # 首页（教授索引 + 赛道网络 + 博士生名单）
├── professor.html            # 教授详情页
├── README.md
├── data/
│   └── professors.js         # 教授 / 博士生 / 院系 / 赛道 数据
├── assets/
│   ├── style.css             # 浅色苹果风样式
│   ├── charts.js             # 3 个图表（赛道网、方向热度、院系密度）
│   └── main.js               # 主页交互（筛选 / 搜索 / 渲染）
└── _shared/
    ├── js/echarts.min.js     # ECharts 图表库
    └── fonts/                # WorkSans / InstrumentSans / IBMPlexMono
```

## 数据来源

- 3 份内部 Mapping 报告（2026.6.29 编）
- IIIS 官方 ICRA 2024 成果合辑
- 清华自动化系 / 智能产业研究院（AIR）/ 软件学院 公开新闻
- 公开学术新闻 / arXiv 检索结果

## 免责声明

本工具仅用于 VC 内部投研参考；融资额、估值、持股等数据来自公开报道，时效以官方披露为准。
