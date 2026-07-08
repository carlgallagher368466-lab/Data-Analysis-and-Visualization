# Student Game Performance EDA

本项目基于 Kaggle 竞赛数据集 **Predict Student Performance from Game Play**，完成数据分析课程项目中的数据整理、清洗、预处理、描述性统计、探索性分析和可视化展示。

项目重点不是构建复杂预测模型，而是围绕一个清晰的数据分析问题展开：

> 学生在游戏学习过程中的行为特征，是否能够解释其答题表现差异？

## 项目内容

- 对 `train.csv` 和 `train_labels.csv` 进行读取、抽样、字段解析和会话级特征聚合。
- 计算总体答题正确率、会话正确率、题目难度和阶段正确率。
- 比较高低表现组在事件类型、事件数量、设置行为等方面的差异。
- 引入时间、路径和空间三个高级 EDA 维度：
  - 标准化游戏进程中的行为节奏；
  - 事件类型转移矩阵；
  - 屏幕坐标空间密度图。
- 输出课程报告、汇报 PPT 和可视化图表。

## 目录结构

```text
student-game-performance-eda/
├── notebooks/
│   └── 高级EDA_学生游戏表现分析.ipynb
├── reports/
│   ├── 数据分析与可视化-最终版.docx
│   └── 学生游戏表现高级EDA汇报.pptx
├── figures/
│   ├── fig01.png
│   ├── ...
│   └── fig14_spatial_density.png
├── data/
│   └── README.md
├── requirements.txt
├── .gitignore
└── README.md
```

## 数据来源

数据来自 Kaggle：

[Predict Student Performance from Game Play](https://www.kaggle.com/competitions/predict-student-performance-from-game-play)

由于原始数据文件较大，仓库不包含 `train.csv`、`train_labels.csv`、`test.csv` 或压缩包。请按 `data/README.md` 下载并放置数据。

## 主要结论

1. 整体答题正确率约为 70.6%，但题目之间难度差异明显。
2. Q13 是最突出的困难题，正确率约为 27.5%；Q2 正确率最高，约为 97.9%。
3. 官方阶段 `0-4`、`5-12`、`13-22` 的正确率分别约为 88.0%、65.0%、71.2%，阶段差异显著。
4. 事件数量与平均正确率呈显著负相关，提示更高活跃度不一定代表更好学习效果。
5. 时间进程、事件转移矩阵和空间热区能够补充解释学生的学习过程差异。

## 运行环境

建议使用 Python 3.10 或以上版本。

安装依赖：

```bash
pip install -r requirements.txt
```

打开 Notebook：

```bash
jupyter notebook notebooks/高级EDA_学生游戏表现分析.ipynb
```

## 说明

本项目为课程作业用途，数据仅用于学习与分析。报告和 PPT 已放在 `reports/` 目录中。

