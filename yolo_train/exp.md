# 检测模型训练：
## Data: 2025-06-08
1. 训练v20250604_shuffle(mAP50=0.9) vs v20250506_shuffle(0.9) vs  v20250506_shuffle_align(mAP50=0.6)实验结果，大批量数据远好于小批量数据-->结论：v20250604的验证集更难

2. 训练v20250604(mAP50=0.52) vs v20250506_align(mAP50=0.48), 大批量数据效果更好，但是均发生了过拟合，需要策略缓解过拟合

3. 训练v20250604(mAP50=0.52) vs v20250604_aug(mAP50=0.52), 效果完全一致，应该是数据增强参数没有正确打开

TODO

0. 0604训练，0506测试, 0.95，很高
1. 训练数据shuffle, 结果一致，说明默认shuffle了
3. 5折实验,实验结果依旧过拟合，不是数据划分的问题
4. data aug: 默认开启的
5. 降低模型参数量，从Large 降低到small or medium，依旧过拟合
6. 更改优化器，先更改weight decay系数
