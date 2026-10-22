# 数据集说明（弟弟食物图片分类小作业参考）

以下两个公开数据集的信息均于本次任务中在 Hugging Face 实际查询得到，**数据以查询返回为准**。

---

## 1. Food-101（经典食物图像数据集）

- **名称**：Food-101
- **Hugging Face 仓库**：[ethz/food101](https://huggingface.co/datasets/ethz/food101)
- **作者**：ethz
- **创建 / 最近更新**：2022-03-02 / 2026-03-09
- **许可**：unknown（数据卡未标注）

### 实际查询到的信息

| 项目 | 查询结果 |
|---|---|
| 类别数 | **101 个食物类别**（schema 中 label 为 ClassLabel，含 apple_pie、baby_back_ribs、baklava …… sushi、tacos、takoyaki、tiramisu、tuna_tartare、waffles 等 101 类） |
| 图像总量 | **101,000 张**（每类 750 张训练图 ＋ 250 张人工审核过的测试图） |
| 数据规模（查询返回） | 总计 101.0K 行；`default/train` 75.8K 行（8 个 parquet 文件、3.8 GB）、`default/validation` 25.3K 行（3 个 parquet 文件、1.3 GB） |
| 下载量 | **674.3K** |
| 点赞数 | 158 |
| 任务类型 | image-classification（多类图像分类） |
| 数据格式 | parquet（图像 ＋ 标签两列） |
| 其他说明 | 训练集刻意未清洗、含噪声；所有图片最大边长统一缩放至 512 像素 |

### 用途建议

食物图片分类小作业可直接参考 Food-101 的 101 类类别体系来组织自己的样本集，也可以直接下载其子集做训练 / 测试。

---

## 2. Foods Nutrition Dataset（自选公开食物营养数据集）

- **名称**：Foods Nutrition Dataset
- **Hugging Face 仓库**：[adarshzolekar/foods-nutrition-dataset](https://huggingface.co/datasets/adarshzolekar/foods-nutrition-dataset)
- **作者**：adarshzolekar
- **创建 / 最近更新**：2025-09-10 / 2026-09-08
- **许可**：CC-BY-4.0

### 实际查询到的信息

| 项目 | 查询结果 |
|---|---|
| 样本量 | **1,028 种常见食物条目**（查询返回 `default/train` 1.0K 行、9 列，单个 parquet 文件 62.5 KB） |
| 字段（9 列） | Food Items、Energy kcal、Carbs、Protein(g)、Fat(g)、Freesugar(g)、Fibre(g)、Cholestrol(mg)、Calcium(mg) |
| 下载量 | **2.1K** |
| 点赞数 | 11 |
| 任务类型 | tabular-classification、tabular-regression、table-to-text |
| 数据格式 | csv（表格 / 文本模态） |
| 数据划分 | 单一 train split |

### 用途建议

如果作业还需要「每种食物的营养信息」，可以用这个数据集查能量（kcal）、蛋白质、脂肪、纤维、钙等指标，把图片分类和营养数值结合起来展示。

---

## 两个数据集对比小结

| | Food-101 | Foods Nutrition Dataset |
|---|---|---|
| 数据类型 | 食物图像 | 食物营养表格 |
| 类别 / 条目 | 101 类 | 1,028 条 |
| 样本量 | 101,000 张图（train 75.8K ＋ validation 25.3K） | 1.0K 行 × 9 列 |
| 下载量 | 674.3K | 2.1K |
| 许可 | unknown | CC-BY-4.0 |

> 说明：两个数据集的类别数、样本量、下载量等数字均为本次在 Hugging Face 查询接口返回的实时结果，后续可能随平台更新变化。
