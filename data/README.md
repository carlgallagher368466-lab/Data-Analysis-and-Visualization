# 数据文件说明

本仓库不直接包含 Kaggle 原始数据文件，原因是文件体积较大，不适合上传到 GitHub。

请从 Kaggle 竞赛页面下载数据：

https://www.kaggle.com/competitions/predict-student-performance-from-game-play

下载后建议将文件解压到本目录，结构如下：

```text
data/
├── train.csv
├── train_labels.csv
├── test.csv
└── sample_submission.csv
```

如果 Notebook 中使用的是本地绝对路径，请根据自己的电脑路径修改 `DATA_DIR` 或 `ROOT` 变量。

原始数据文件较大，已被 `.gitignore` 排除：

- `*.csv`
- `*.zip`
- `*.rar`
- Kaggle 原始数据目录

