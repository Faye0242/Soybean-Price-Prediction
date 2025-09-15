# Soybean-Price-Prediction
Soybeans are highly useful for many agricultural industries and companies. In particular, feed companies will use soybean oil and soybean meals to create products. When the feed company purchases soybeans periodically and in a large amount, the significance of soybean price prediction and risk control is obvious. 

This is my personal project based on my interest and past experience in analyzing soybean prices. The skillset used in this project includes: **Excel, Jupyter Notebook(Python), ML models**. This project includes **Web Scrapping, API, EDA(exploratory data analysis), data visualization, machine learning modeling, time-series, and business analyzing reports.**

https://www.moa.gov.cn/ztzl/ddymdzfhjs/mtbd_29066/wenzi/202208/t20220811_6406740.htm

### Project Overview 项目介绍
大豆是中国饲料与食品产业的重要原料，中国进口依赖度超过 80%。在中国市场的应用，中国进口大豆价格通常是 CBOT 期货 + 基差（运费、升贴水、关税、汇率调整）。所以中国企业虽然最终买的是 现货大豆，但价格基准往往来自 CBOT 期货。
本项目结合 **国际期货市场数据（CBOT）**、**美国 USDA 出口数据** 和 **中国海关进口数据**，研究CBOT大豆价格波动对中国进口成本的传导效应，并提出风险管理商业建议。

<ins>Stakeholder</ins>: 中国大中小型饲料企业

<ins>痛点</ins>: 饲料企业进口依赖巴西/美国，价格波动直接影响成本，如何通过期货市场信号预测中国进口价格走势

<ins>分析价值</ins>：预测大豆价格走势，提出采购和风险对冲策略，建立价格传导模型，给出套利/对冲机会



### Data Collection & Preprocessing
历史大豆进出口量，及 CBOT大豆期货价格数据
  1. CBOT 大豆期货（Chicago Board of Trade）价格：             Yahoo Finance
  2. 2020年-2025年中国海关的大豆进口数据：              中国海关统计官网， http://stats.customs.gov.cn
  3. 美国出口到中国的大豆及其制品的数量（Qty）和价值（Value）：         USDA

特征工程：加入宏观经济指标（美元指数、原油价格）、气候因素（降雨量、温度）、季节性 Dummy 变量

### 探索性数据分析 (EDA)

趋势分析：价格走势、季节性模式

相关性分析：大豆价格 vs 原油、玉米、小麦价格

波动性分析：标准差、移动平均

### 建模 (Modeling)

统计模型：ARIMA、SARIMAX（考虑季节性、宏观变量）

机器学习模型：XGBoost、LSTM（深度学习时间序列预测）

### 数据可视化 Visualization & Dashboard

预测 vs 实际对比折线图

风险预警仪表盘（价格上涨概率、波动区间）

不同情景的采购成本模拟

### 商业分析 (Business Analysis)

采购策略建议：在预测上涨时提前锁定价格；下跌趋势时延后采购

风险控制：利用预测结果进行期货对冲（hedging）

敏感性分析：原油上涨 10% 对大豆价格的传导效应

1. 商业分析层次（推荐给你用）

逻辑：国际大豆期货价格上涨 → 中国进口成本上升 → 饲料企业利润受压缩。

对策：企业可以通过：

提前签订远期合同

在 CBOT 上买入大豆期货/期权进行对冲

在价格低位时增加库存

价值：展示你能把预测结果转化成 可执行的商业政策。
2. 量化研究层次（如果你想展示技术力）

逻辑：利用中国进口均价 vs 美国期货价格的差异，构建一个“跨市场价差”。

策略：

如果进口均价长期高于期货价格 → 提示套利空间

如果价差扩大/收窄 → 信号触发对冲操作

技术：用 Python 回测（pandas + 交互式plotly），简单展示策略效果。

价值：展示你有 量化分析的潜力，但不需要做到实盘交易的程度。

# 结论 (Conclusion & Business Value)

模型预测准确度

对企业的 ROI 提升

后续优化方向（增加天气数据、引入全球市场指标）
