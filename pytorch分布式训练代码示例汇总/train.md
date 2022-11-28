## 单机单卡
- 模型拷贝 model.cuda()
- 数据拷贝（每步） data.cuda()
- 判断cuda 可用
- 模型保存与加噪 torch.save 模型 优化器 其他变量 torch.load 




##  单机多卡
- 检测GPU数目 torch.cuda.device_count()
- 命令行 cuda_visible_devices = ‘’限制
### 现在 torch.nn.parallel.DistributedDataParallel (DDP) 多进程执行多卡训练，效率高
- gpu之间通信方式 nccl，world_size 当前电脑上的gpu数量 rank 是在几个gpu上