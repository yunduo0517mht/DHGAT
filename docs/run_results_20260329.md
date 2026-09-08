# 跑测记录 - 2026-03-29

## 运行参数

| 参数 | 值 |
|------|-----|
| `g_features` | `['speaker', 'context']` |
| `decision_feature` | `speaker` |
| `num_iterations` | 1 |
| `num_epochs` | 200 |
| `train_percent` | 0.3 (30%) |
| `l1` | 0.7 |
| `l2` | 0.1 |
| `hidden_size` | 256 → 128（两层） |
| `lr` | 0.001 |
| `dropout` | 0.5 |
| `optimizer` | Adam |
| `output_size` | 6（6分类） |

## 收敛过程

| 轮数 | Test ACC |
|------|---------|
| 50   | 39.73%  |
| 100  | 43.77%  |
| 200  | 44.35%  |

> 约 111 轮达到峰值（Best Val ACC: 44.56%），之后趋于平稳。

## 最终测试结果

| 指标 | Train | Test |
|------|-------|------|
| **Accuracy** | 31.97% | **44.35%** |
| **Macro F1** | 29.29% | 42.67% |
| **Micro F1** | 31.97% | 44.35% |
| **Macro Precision** | 46.32% | 54.41% |
| **Micro Precision** | 31.97% | 44.35% |
| **Macro Recall** | 30.16% | 42.48% |
| **Micro Recall** | 31.97% | 44.35% |

## 结果文件

`results/results_labeled30pct_iter1_epochs200_featspeaker-context_20260329_200941.csv`
