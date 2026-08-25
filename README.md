# 淘宝用户行为数据分析

基于 PySpark + MySQL 的亿级用户行为日志 ETL 清洗与统计分析

![Python](https://img.shields.io/badge/Python-3.6-blue)
![PySpark](https://img.shields.io/badge/PySpark-3.2.4-orange)
![MySQL](https://img.shields.io/badge/MySQL-9.7-blue)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen)

---

## 📖 项目简介

本项目基于阿里天池公开数据集 **UserBehavior**，使用 **PySpark** 对 **超1百万条** 淘宝用户行为日志进行 ETL 清洗与统计分析。通过 Spark SQL 完成核心指标（日活跃购买用户 UV、日订单量）计算，并将结果持久化至 **MySQL** 数据库，最后使用 **Matplotlib** 进行可视化呈现。

---

## 🛠️ 技术栈

- **Python 3.6**
- **PySpark 3.2.4**（大数据离线处理）
- **MySQL 9.7**（结果存储）
- **Matplotlib / Pandas**（数据可视化）
- **Jupyter Notebook**（交互式开发）

---

## 📂 数据来源

- **数据集**：UserBehavior（淘宝用户行为数据集）
- **来源**：阿里天池（Tianchi）
- **数据量**：超1百万条用户行为日志
- **字段**：user_id, item_id, category_id, behavior_type, timestamp
- **行为类型**：pv（点击）、buy（购买）、cart（加购）、fav（收藏）

---

## 📊 数据分析与洞察

通过 PySpark 对数据进行预处理（时间戳格式化、行为类型过滤），统计了**每日活跃购买用户（UV）** 和 **日订单量**，发现：

- **周末效应明显**：12月2日-3日（周末）UV 环比增长约 **24%**，订单量同步增长约 **22%**
- **日均订单量**：约 22 万单
- **日均独立购买用户**：约 14.7 万人

> 运营建议：可在周末加大活动投放力度，提升转化效率。

---

## 📁 文件说明

| 文件名 | 说明 |
|--------|------|
| `taobao_user_behavior_analysis.ipynb` | Jupyter Notebook 完整代码（ETL + 统计 + 入库） |
| `daily_uv_sales_trend.png` | 双轴趋势图（UV + 订单量可视化） |

---

## 🏗️ 项目结构
taobao-user-behavior-analysis/
├── taobao_user_behavior_analysis.ipynb # 主代码文件
├── daily_uv_sales_trend.png # 可视化图表
├── .gitignore # Git 忽略文件配置
└── README.md # 项目说明

---

## 🚀 如何运行

1. **配置环境**：
   - Java 11 / PySpark 3.2+ / MySQL 9.7+
   - 安装依赖：`pip install pyspark pandas matplotlib sqlalchemy pymysql`

2. **下载数据**：
   - 从阿里天池下载 UserBehavior.csv（超1百万条）

3. **修改配置**：
   - 在代码中修改 MySQL 用户名和密码

4. **运行代码**：
   - 启动 Jupyter Notebook：`jupyter notebook`
   - 打开 `.ipynb` 文件，依次执行所有单元格

---

## 👤 作者信息

- **邮箱**：1158583571@qq.com
- **GitHub**：[https://github.com/Natsu-Reisa](https://github.com/Natsu-Reisa)

---

## 📄 许可证

本项目仅供学习与求职展示使用，数据来源于阿里天池公开数据集。
