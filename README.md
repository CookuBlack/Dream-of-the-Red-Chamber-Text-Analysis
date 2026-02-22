# 红楼梦文本数据分析

# Dream of the Red Chamber Text Analysis

<div align="center">
  <p>基于Python的《红楼梦》文本数据处理与可视化分析项目 | A Python-based text data processing and visualization analysis project for "Dream of the Red Chamber"</p>
</div>

![logo](./assets/logo.png)

---

## 项目简介 | Project Introduction

该仓库记录的是笔者大学期间的Python期末考核实战项目，以古典名著《红楼梦》为分析对象，实现了文本数据的清洗、处理与多维度可视化分析。

本项目仅作为**学习参考**用途，代码实现偏向基础实战，可能存在优化空间，笔者开源的初衷是留存学习笔记、方便日后复盘，也希望能为初学Python数据分析的同学提供参考案例。

> This repository records the author's Python final assessment project during college, taking the classic masterpiece "Dream of the Red Chamber" as the analysis object, and realizing the cleaning, processing and multi-dimensional visual analysis of text data.
> 
> This project is only for **learning reference** purposes, the code implementation is biased towards basic practical combat and may have room for optimization. The author's original intention of open source is to keep study notes for future review, and also hope to provide reference cases for students who are new to Python data analysis.


## 环境配置 | Environment Configuration
### 基础要求 | Basic Requirements
- Python 版本：3.8.0 及以上（推荐 3.8.x ~ 3.10.x，兼容性更佳）
- Python Version: 3.8.0 and above (3.8.x ~ 3.10.x is recommended for better compatibility)

### 依赖安装 | Dependency Installation
1. 确保已安装 `pip` 包管理工具
2. 执行以下命令安装项目依赖（需提前创建 `requirements.txt` 文件，内容见下方）：
```bash
pip install -r requirements.txt
```

### 推荐依赖清单 | Recommended Dependency List
创建 `requirements.txt` 文件并写入以下内容：
```txt
# 基础数据处理
pandas>=1.5.3
numpy>=1.24.3

# 文本处理
jieba>=0.42.1
chardet>=5.2.0

# 数据可视化
pyecharts>=2.0.3
wordcloud>=1.9.2
matplotlib>=3.7.2
seaborn>=0.12.2

# 辅助工具
beautifulsoup4>=4.12.2
requests>=2.31.0
```


## 项目结构 | Project Structure
```
├── 红楼梦文本.txt                # 核心数据源：《红楼梦》原始文本文件
│                                  Core data source: Original text file of "Dream of the Red Chamber"
├── DataProcessing.py             # 数据处理主文件：文本清洗、分词、数据提取等核心逻辑
│                                  Main data processing file: Core logic for text cleaning, word segmentation, data extraction, etc.
├── ConformAllChart.py            # 可视化汇总文件（主运行文件）：将所有图表整合到单个HTML页面
│                                  Visualization summary file (main running file): Integrate all charts into a single HTML page
├── Chart/                        # 可视化输出目录：存放生成的所有图表HTML源码文件
│                                  Visualization output directory: Store all generated chart HTML source files
├── # 以下为单图表调试文件 | The following are single chart debugging files
├── BarLine.py                    # 柱状图+折线图：多维度数据对比可视化
│                                  Bar chart + Line chart: Multi-dimensional data comparison visualization
├── Pie.py                        # 空心饼图：类别占比分析
│                                  Hollow pie chart: Category proportion analysis
├── RadialTree.py                 # 辐射树图：人物/情节层级关系展示
│                                  Radial Tree Diagram: Display of character/plot hierarchical relationships
├── Relation.py                   # 关系图：人物互动/关联分析
│                                  Relation chart: Character interaction/association analysis
├── TimeLinePie.py                # 时间线饼图：时序维度占比变化分析
│                                  Timeline Pie Chart: Analysis of proportion changes in time dimension
├── WordCloud.py                  # 词云图：核心词汇/高频词可视化
│                                  Word cloud chart: Core vocabulary/high-frequency word visualization
├── requirements.txt              # 环境依赖清单
│                                  Environment dependency list
└── README.md                     # 项目说明文档
                                  Project description document
```


## 运行说明 | Running Instructions
### 核心流程 | Core Process
1. **数据预处理**：先运行 `DataProcessing.py`，完成《红楼梦》文本的清洗、分词等预处理，生成分析用的结构化数据；
   First run `DataProcessing.py` to complete the cleaning and word segmentation of the "Dream of the Red Chamber" text, and generate structured data for analysis.
2. **可视化生成**：
   - 调试单个图表：直接运行对应图表文件（如 `WordCloud.py`、`Pie.py`），生成单个HTML图表文件至 `Chart/` 目录；
   - 整合所有图表：运行 `ConformAllChart.py`，自动汇总所有图表到一个HTML页面，方便统一查看。
   - Debug a single chart: Run the corresponding chart file (e.g., `WordCloud.py`, `Pie.py`) directly to generate a single HTML chart file to the `Chart/` directory;
   - Integrate all charts: Run `ConformAllChart.py` to automatically summarize all charts into one HTML page for easy unified viewing.

### 注意事项 | Notes
- 运行前确保 `红楼梦文本.txt` 文件路径正确，避免文件找不到的报错；
- 部分可视化图表（如词云）可能需要配置中文字体，需根据本地环境调整字体路径；
- 若运行报错，优先检查Python版本和依赖包版本是否匹配。
- Ensure the path of `红楼梦文本.txt` is correct before running to avoid errors of file not found;
- Some visualization charts (such as word cloud) may need to configure Chinese fonts, and the font path needs to be adjusted according to the local environment;
- If an error occurs during running, first check whether the Python version and dependency package versions match.


## 免责声明 | Disclaimer
1. 本项目仅为大学期末考核练习作品，代码质量并非工业级标准，仅供学习参考，请勿用于商业用途；
2. 项目中使用的《红楼梦》文本仅作为学习分析素材，请勿用于任何侵权场景；
3. 因使用本项目代码导致的环境配置、运行报错等问题，作者不承担相关责任。

1. This project is only a practice work for college final assessment, and the code quality is not industrial-grade standard. It is for learning reference only and shall not be used for commercial purposes;
2. The "Dream of the Red Chamber" text used in the project is only for learning and analysis materials, and shall not be used for any infringement scenarios;
3. The author shall not be liable for environmental configuration, runtime errors and other problems caused by the use of the project code.


## 补充说明 | Supplementary Notes
本项目是初学Python数据分析的实战练习，核心侧重：
- 文本数据的基础处理流程（清洗、分词、结构化）；
- 多种可视化图表的实现与整合；
- 从单一文件到多模块协作的基础工程化思路。

如果有优化建议或问题，欢迎交流探讨。

This project is a practical exercise for beginners of Python data analysis, focusing on:
- Basic processing flow of text data (cleaning, word segmentation, structuring);
- Implementation and integration of multiple visualization charts;
- Basic engineering ideas from a single file to multi-module collaboration.

If you have optimization suggestions or questions, welcome to communicate and discuss.


### 总结
1. 完善后的README兼顾中英文版本，结构规范（含项目简介、环境配置、运行说明等核心模块），符合开源项目文档的通用标准；
2. 补充了关键的依赖清单、运行流程和注意事项，降低了使用者的上手成本；
3. 明确了项目的学习属性和免责声明，边界清晰且符合合规要求。
