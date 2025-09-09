# Soybean-Price-Prediction
Soybean is highly useful for many agricultural industries and companies. Especially, feed company will use soybean oil and Soybean meal to create products. When the feed company purchase soybean periodically and in a large amount, the significance of soybean price prediction and risk control is obvious. 
This is my personal project based on my interest and past experience in analyzing soybean price. The skillset used in this project includes: Excel, Jupyter Notebook(Python), ML models, and Tableau. 
This project includes web scrapping, EDA(exploratory data analysis), data visualization, machine learning modeling, time-series, and business analyzing reports.

### Project Overview 项目介绍
Predict future soybean prices (in areas such as agriculture, feed, food, and futures markets), and provide actionable business insights.

### Data Collection & Preprocessing
数据来源：历史大豆价格数据（期货市场 / USDA / Wind / Yahoo Finance 等）

时间区间 & 频率（日/周/月）

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

# 结论 (Conclusion & Business Value)

模型预测准确度

对企业的 ROI 提升

后续优化方向（增加天气数据、引入全球市场指标）
