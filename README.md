# Project Repository: "Extracranial and Intracranial EEG Evidence of Escape Strategies Under Continuous Threat"

This repository contains the data analysis and visualization code for the study "Extracranial and Intracranial EEG Evidence of Escape Strategies Under Continuous Threat." The structure is organized to reflect the key components of the research: behavioral analysis, scalp EEG (Study 1), and intracranial SEEG (Study 2).

## Repository Overview

**Study Title:** Extracranial and Intracranial EEG Evidence of Escape Strategies Under Continuous Threat

**Authors:** [Haoming Zhang, xxxx]

**Publication Status:** [Under Review / In Preparation]

**Last Updated:** October 2025

## 1. Repository Directory Structure

Continuous-Escape-Strategies-EEG-SEEG/
├── README.md                          # 项目主文档（本文档）
├── LICENSE                            # MIT许可证文件
├── CITATION.cff                       # 引用格式文件
├── requirements.txt                   # Python依赖包列表
├── environment.yml                    # Conda环境配置文件
├── run_pipeline.py                    # 主运行脚本
├── data/                              # 数据目录（Git LFS管理）
│   ├── behavioral/                    # 行为学数据
│   │   ├── study1_eeg_metrics.csv     # 研究1（EEG）行为指标
│   │   ├── study2_seeg_metrics.csv    # 研究2（SEEG）行为指标
│   │   └── README_data.md             # 数据说明文档
│   └── neural/                        # 神经影像数据
│       ├── eeg/                       # 头皮EEG数据
│       │   ├── raw/                   # 原始EEG数据（.fif格式）
│       │   ├── preprocessed/          # 预处理后数据
│       │   │   ├── study1_tfr_power.mat
│       │   │   └── study1_epochs.fif
│       │   └── derivatives/           # 衍生数据
│       │       └── theta_alpha_features.csv
│       └── seeg/                      # 颅内SEEG数据
│           ├── raw/                   # 原始SEEG数据（.edf/.mat格式）
│           ├── preprocessed/          # 预处理后数据
│           │   ├── study2_hga_results.mat
│           │   └── study2_roi_labels.mat
│           └── derivatives/           # 衍生数据
│               └── hga_features.csv
├── analysis/                          # 分析脚本目录
│   ├── 01_behavioral/                 # 行为学分析
│   │   ├── behavioral_study1.py       # 研究1行为分析
│   │   ├── behavioral_study2.py       # 研究2行为分析
│   │   ├── behavioral_stats.py        # 统计检验
│   │   └── plot_behavioral.py         # 行为图绘制
│   ├── 02_eeg_study1/                 # EEG研究分析
│   │   ├── preprocess_eeg.py          # EEG预处理
│   │   ├── eeg_tfr_analysis.py        # 时频分析
│   │   ├── eeg_topography.py          # 地形图绘制
│   │   ├── eeg_regression.py          # 回归分析
│   │   ├── theta_gamma_coupling.py    # Theta-Gamma耦合分析
│   │   └── config_eeg.yaml            # EEG分析配置
│   ├── 03_seeg_study2/                # SEEG研究分析
│   │   ├── preprocess_seeg.py         # SEEG预处理
│   │   ├── seeg_hga_analysis.py       # HGA分析
│   │   ├── seeg_roi_analysis.py       # ROI分析
│   │   ├── seeg_connectivity.py       # 连接性分析
│   │   ├── seeg_behavior_link.py      # 神经-行为关联
│   │   └── config_seeg.yaml           # SEEG分析配置
│   └── 04_integrated_analysis/        # 整合分析
│       ├── cross_modal_integration.py # 跨模态整合
│       ├── network_analysis.py        # 网络分析
│       └── meta_analysis.py           # 元分析
├── notebooks/                         # Jupyter Notebooks
│   ├── 01_Behavioral_Exploration.ipynb
│   ├── 02_EEG_Analysis_Pipeline.ipynb
│   ├── 03_SEEG_Analysis_Pipeline.ipynb
│   └── 04_Integrated_Findings.ipynb
├── utils/                             # 工具函数
│   ├── __init__.py
│   ├── data_loader.py                 # 数据加载器
│   ├── plot_utils.py                  # 绘图工具
│   ├── stats_utils.py                 # 统计工具
│   ├── neuro_utils.py                 # 神经影像工具
│   └── file_utils.py                  # 文件操作工具
├── config/                            # 配置文件
│   ├── analysis_params.yaml           # 分析参数配置
│   ├── plot_styles.yaml               # 绘图样式配置
│   └── paths.yaml                     # 路径配置
├── tests/                             # 测试文件
│   ├── test_behavioral.py
│   ├── test_eeg_analysis.py
│   ├── test_seeg_analysis.py
│   └── test_utils.py
├── docs/                              # 文档目录
│   ├── index.md                       # 文档首页
│   ├── installation.md                # 安装指南
│   ├── tutorial.md                    # 使用教程
│   ├── api_reference.md               # API参考
│   └── figures/                       # 文档用图
├── figures/                           # 生成图表
│   ├── behavioral/                    # 行为学图表
│   │   ├── figure1/                   # 图1相关
│   │   │   ├── panel_a.png
│   │   │   ├── panel_b.png
│   │   │   └── panel_c.png
│   │   └── supplementary/
│   ├── eeg/                           # EEG图表
│   │   ├── figure2/
│   │   │   ├── topography.png
│   │   │   ├── tfr_plot.png
│   │   │   └── regression.png
│   │   └── supplementary/
│   ├── seeg/                          # SEEG图表
│   │   ├── figure3/
│   │   │   ├── hga_timecourse.png
│   │   │   ├── roi_comparison.png
│   │   │   └── behavior_correlation.png
│   │   └── supplementary/
│   └── integrated/                    # 整合分析图表
│       ├── figure4/
│       └── supplementary/
├── results/                           # 分析结果
│   ├── statistical_tests/             # 统计检验结果
│   │   ├── behavioral_stats.csv
│   │   ├── eeg_stats.csv
│   │   └── seeg_stats.csv
│   ├── model_outputs/                 # 模型输出
│   │   ├── regression_models.pkl
│   │   ├── clustering_results.npy
│   │   └── network_metrics.csv
│   └── summary_tables/                # 汇总表格
│       ├── demographic_summary.csv
│       ├── behavioral_summary.csv
│       └── neural_summary.csv
├── manuscript/                        # 论文相关文件
│   ├── main_manuscript.tex            # 主论文LaTeX
│   ├── supplementary.tex              # 补充材料
│   ├── references.bib                 # 参考文献
│   └── responses/                     # 审稿回复
└── .github/                           # GitHub配置
    ├── workflows/                     # CI/CD工作流
    │   ├── tests.yml                  # 测试工作流
    │   └── build_docs.yml             # 文档构建工作流
    └── ISSUE_TEMPLATE/                # Issue模板

## 2. File Descriptions

| Directory/File | Description | 中文描述 |
|----------------|-------------|----------|
| `README.md` | Main documentation file | 主文档 |
| `LICENSE` | License information | 许可证信息 |
| `requirements.txt` | Python package dependencies | Python包依赖 |
| `environment.yml` | Conda environment specification | Conda环境配置 |
| `data/` | Contains all anonymized input data and preprocessed results | 匿名化输入数据和预处理结果 |
| `data/behavioral/` | Behavioral metrics (Reaction Time, Freeze Ratio, Escape Tendency) | 行为指标（反应时间、冻结率、逃跑倾向） |
| `data/eeg_seeg/` | Preprocessed neural activity data for EEG and SEEG | 预处理后的EEG和SEEG神经活动数据 |
| `analysis/` | Core analysis scripts for statistical analysis and visualization | 核心统计分析脚本 |
| `01_behavioral_analysis/` | Scripts for analyzing escape metrics and predator type effects | 分析逃跑指标和捕食者类型效应的脚本 |
| `behavioral_study1.py` | Code for analyzing and plotting Study 1 (EEG) behavioral results | 研究1（EEG）行为结果分析和绘图代码 |
| `behavioral_study2.py` | Code for analyzing and plotting Study 2 (SEEG) behavioral results | 研究2（SEEG）行为结果分析和绘图代码 |
| `02_eeg_study1/` | Analysis scripts for scalp EEG data (Theta/Alpha power) | 头皮EEG数据（Theta/Alpha功率）分析脚本 |
| `eeg_tfr_analysis.py` | Time-Frequency Analysis for theta/alpha power differences | 时频分析代码，用于计算功率差异 |
| `eeg_topography_plotting.py` | Code to plot topographic maps of theta power differences | 绘制Theta功率差异地形图的代码 |
| `eeg_regression_model.py` | Multiple linear regression models for trial-level analysis | 多重线性回归模型，用于试验级分析 |
| `03_seeg_study2/` | Analysis scripts for intracranial SEEG data (HGA) | 颅内SEEG数据（HGA）分析脚本 |
| `seeg_hga_analysis.py` | Extraction and comparison of High Gamma Activity (70-120 Hz) | 提取和比较高伽马活动的脚本 |
| `seeg_roi_plotting.py` | Code to plot HGA time courses in selected ROIs | 绘制选定脑区HGA时程的代码 |
| `seeg_hga_behavior_link.py` | Scripts linking HGA to trial-by-trial Escape Tendency | 将HGA与试验级逃跑倾向联系起来的脚本 |
| `notebooks/` | Jupyter notebooks for interactive data exploration | 交互式数据探索的Jupyter笔记本 |
| `utils/` | Utility functions and helper modules | 工具函数和辅助模块 |
| `config/` | Configuration files for analysis parameters | 分析参数配置文件 |
| `figures/` | Stores output images generated by analysis scripts | 存储分析脚本生成的输出图像 |



## 3.Key Analysis Code Snippets (Conceptual Python/MATLAB)

The following conceptual code outlines the core analyses described in the paper.

3.1. Behavioral Analysis (Study 1 & 2 Replication)

This script analyzes key behavioral metrics (Escape Reaction Time, Escape Tendency, Freeze Ratio) and visualizes the significant differences between Direct and Divert attacks.
