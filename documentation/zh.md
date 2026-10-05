<!-- ELUCENIA technical documentation · escore-de-rockall · zh · no clinical/professional/rights approval -->

# Rockall 评分

[条件、来源与许可](https://elucenia.org/zh/tools/escore-de-rockall)

## 使用方法

在门户中使用工具，或通过本地 HTTP 服务器打开 index.html。选择语言，填写各字段，然后计算。

## 输入与单位

### 年龄

`idade`

- `0` — \< 60 岁
- `1` — 60 至 79 岁
- `2` — ≥ 80 岁

### 休克

`choque`

- `0` — 无休克（收缩压≥100且心率\<100）
- `1` — 心动过速（收缩压≥100且心率≥100）
- `2` — 低血压（收缩压\<100 mmHg）

### 合并症

`comorb`

- `0` — 无重要合并症
- `2` — 心力衰竭、缺血性心脏病或其他重要合并症
- `3` — 肾衰竭、肝衰竭或播散性癌症

### 内镜诊断

`diag`

- `0` — Mallory-Weiss或无病变（无出血征象）
- `1` — 所有其他诊断
- `2` — 上消化道肿瘤
- `na` — 尚未行内镜检查

### 近期出血征象

`estigma`

- `0` — 无，或仅有黑色斑点（酸性血红素）
- `2` — 上消化道内有血、附着血块、可见血管或喷射性出血
- `na` — 尚未行内镜检查

## 方法版本

Rockall 1996：内镜前0–7，完整0–11；不与GBS混淆

## 已记录的公式

内镜前（0至7）：年龄（0至2）+休克（0至2）+合并症（0、2或3）。

完整（0至11）：再加诊断（0至2）及近期出血征象（0或2）。

## 限制与适用人群

1996年的Rockall评分在年龄大于16岁的急性上消化道出血者中研究。完整版本依赖诊断及内镜出血征象；内镜前版本不包含这些信息。分层有助于考虑处理方式，但不能确定个体出院的安全性或不会再出血。

## 参考文献

- [Rockall TA et al. Risk assessment after acute upper gastrointestinal haemorrhage. Gut, 1996.](https://doi.org/10.1136/gut.38.3.316)

- [Stanley AJ et al. Comparison of risk scoring systems for patients presenting with upper gastrointestinal bleeding: international multicentre prospective study. BMJ, 2017.](https://doi.org/10.1136/bmj.i6432)

## 复现技术测试

在此仓库的根目录中运行 node test.cjs，以重复已记录的合成案例。原始输入、预期结果和容差保持不变。技术测试不构成临床验证。

```sh
node test.cjs
```

tool.json 包含来源、版本和审查范围。examples.json 保留合成输入与预期结果；results.json 记录实际得到的结果。

[记录与参考文献](../tool.json) · [JavaScript代码](../calculator.js) · [参考案例](../examples.json) · [results.json](../results.json)

## 审查与使用条件

尚未开展独立临床审查。

此界面为自主编写的翻译，并非官方或认证版本。尚未完成独立临床审查、专业语言审查或工具权利授权。

公式或分类结果。解释、处理及适用性须结合专业评估和所选来源。

## 许可与署名

Apache-2.0 仅适用于 ELUCENIA 代码。工具、出版物、翻译和数据的权利仍归各自权利人所有。请保留 LICENSE 和 NOTICE。

ELUCENIA · Felipe Guedes · Copyright © 2026
