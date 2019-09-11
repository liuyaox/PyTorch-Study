# PyTorch API Doc

# 0. Overview

# 1. torch.nn

## 1.1 Overview

#### Article

- [PyTorch 中，nn 与 nn.functional 有什么区别](https://www.zhihu.com/question/66782101)


## 1.2 nn.LSTM

返回的output, (h_n, c_n)

![](https://raw.githubusercontent.com/liuyaox/ImageHosting/master/for_markdown/PyTorch-LSTM.png)

纵向(各Layer)的凝聚：output comprises all the hidden states in the last layer (last depth-wise, not time-wise)

横向(各Timestep)的凝聚：(h_n, c_n) comprises the hidden states in the last timestep, so you could potentially feed them into another LSTM

当num_layers=1时，output和hidden相等（等一哈，难道不是output[seq_len-1]=sofxmax(hidden)???）


# 2. torch.nn.utils

## 2.1 nn.utils.rnn

### 2.1.1 pad_sequence & pack_padded_sequence & pad_packed_sequence

处理变长序列，功能目的类似于Keras中的pad_sequence和Masking，但实现机制不同

```python
# 同Keras中的pad_sequence
torch.nn.utils.rnn.pad_sequence()

# 将多余的<PAD>去除，获得一个干净的、最初的序列，随后便可输入至LSTM中，类似于Keras中的Masking
torch.nn.utils.rnn.pack_padded_sequence()

-- 参数列表：
  -- input: 有 <PAD> 的 batch 序列
  -- lengths: input 中每个序列的长度
  -- batch_first: 如果为True， input 必须是 [batch_size, seq_len, input_size], 参见LSTM
  -- enforce_sorted: 如果为True， 那么 input 中的序列需要按照 长度递减排列

-- 返回值：
    一个 PackedSequence 对象

# LSTM处理后，需要对Pack后的信息进行Pad，本质上是将数据从PackedSequence转化为Tensor
torch.nn.utils.rnn.pad_packed_sequence()

-- 参数列表：
  -- sequence： 一个PackedSequence对象
  -- batch_first: 
  -- padding_value: padding该序列的values
  -- total_length: Padding到多长， 一般为None

-- 返回值：
  -- output: 有 padding 信息的序列输出
  -- output_lengths: 每个序列没有Padding之前的长度
```

顺序: Origianl Tensor -> pad_sequence -> Embedding -> pack_padded_sequence -> LSTM -> pad_packed_sequence -> 后续环节比如Attention

#### Reference

- <https://github.com/HarshTrivedi/packing-unpacking-pytorch-minimal-tutorial>

- [PyTorch 训练 RNN 时，序列长度不固定怎么办？ - 2019](https://zhuanlan.zhihu.com/p/59772104)

