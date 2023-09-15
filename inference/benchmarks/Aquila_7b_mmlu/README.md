### 1. 推理数据集
> Download website：https://paperswithcode.com/dataset/mmlu

We use Validation Images:
| Dataset                       | FileName               | Size  | Checksum                              |
| ----------------------------- | ---------------------- | ----- | ------------------------------------- |
| MMLU | MMLU | 320M | / |


### 2. 模型与权重

* 模型实现
  * 运行自动下载
* 权重下载
  * 运行自动下载

### 2. 软硬件配置与运行信息参考

#### 2.1 Nvidia A100


- ##### 优化策略

   - None

- ##### 并行策略

   - None

- ##### 硬件环境
    - 机器、加速卡型号: NVIDIA_A100-SXM4-40GB
    - 多机网络类型、带宽: InfiniBand，200Gb/s
    
- ##### 软件环境
   - OS版本：Ubuntu 20.04
   - OS kernel版本: 5.4.0-113-generic
   - 加速卡驱动版本：470.129.06
   - Docker 版本：20.10.16
   - 训练框架版本：pytorch-1.13.0a0+937e930
   - 依赖软件版本：
     - cuda: 11.8

   
- 推理工具包
   - None

### 3. 运行情况




* 指标列表

| 指标名称           | 指标值索引       | 特殊说明                                     |
| ------------------ | ---------------- | -------------------------------------------- |
| 数据精度           | precision        | 可选fp32/fp16                                |
| 批尺寸             | bs               |                                              |
| 硬件存储使用       | mem              | 通常称为“显存”,单位为GiB                     |
| 端到端时间         | e2e_time         | 总时间+Perf初始化等时间                      |
| 验证总吞吐量       | p_val_whole      | 实际验证token数除以总验证时间                 |
| 验证计算吞吐量     | p_val_core       | 不包含IO部分耗时                             |
| 推理总吞吐量       | p_infer_whole    | 实际推理token数除以总推理时间                 |
| **推理计算吞吐量** | **\*p_infer_core** | 不包含IO部分耗时                             |
| 推理结果           | acc(推理/验证)   | MMLU回答准确率（few_shots:5）                   |

* 指标值

| 推理工具  | precision | bs   | e2e_time | p_val_whole | \*p_val_core | p_infer_whole | \*p_infer_core |\*MFU| acc         | mem        |
| ----------- | --------- | ---- | -------- | ----------- | ---------- | ------------- | ------------ |  ------------ |----------- | ---------- |
| tensorrt | fp16   | 1  | 1333.664   |   6988.69   |  7212.94  | /    | / |32.4%| 0.33 | 30.0/40.0 |