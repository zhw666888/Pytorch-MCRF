# Pytorch-MCRF
关于Masked-CRF的pytorch版本实现

本版本实现基于开源的pytorch-crf==0.7.2版本

Masked的改进策略参见论文：

Masked Conditional Random Fields for Sequence Labeling[https://arxiv.org/abs/2103.10682]

tensorflow版本的实现，请参见作者提供的代码：
https://github.com/DandyQi/MaskedCRF

注意，本文使用方法基本与pytorch-crf的使用方法一致
【https://pytorch-crf.readthedocs.io/en/stable/index.html】，
但是如下使用：
self.crf = CRF(num_tags=self.num_seq_labels, batch_first=True, label2idx=label2id)

需要传入label2idx参数，如：

label2id = {
     "O": 0,
     "B-PER": 1,
     "B-LOC": 2,
     "B-ORG": 3,
     "I-PER": 4,
     "I-LOC": 5,
     "I-ORG": 6,
 }

欢迎交流
