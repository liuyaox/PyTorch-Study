# PyTorch Overview

Overview, Courses, Code, Books, Misc., etc.

#### Paper

- [PyTorch: An Imperative Style, High Performance Deep Learning Library - 2019](https://papers.nips.cc/paper/9015-pytorch-an-imperative-style-high-performance-deep-learning-library.pdf)

    **Chinese**: [NeurIPS顶会接收，PyTorch官方论文首次曝光完整设计思路](https://mp.weixin.qq.com/s?__biz=MzA3MzI4MjgzMw==&mid=2650775275&idx=1&sn=e0fc05636689fc6a2aaeb63e57884c47)


#### Github

- <https://github.com/Cadene/pretrained-models.pytorch>

    Pretrained ConvNets for pytorch: NASNet, ResNeXt, ResNet, InceptionV4, InceptionResnetV2, Xception, DPN, etc.

    The goal of this repo is:

    - to help to reproduce research papers results (transfer learning setups for instance)

    - to access pretrained ConvNets with a unique interface/API inspired by torchvision

- [PyTorch Cookbook（常用代码段整理合集)](<https://zhuanlan.zhihu.com/p/59205847?>)

- <https://github.com/intermt/awesome-pytorch-chinese>

    史上最全PyTorch资源汇总：教程、实战、必读论文、中文教材一应俱全

- <https://github.com/bharathgs/Awesome-pytorch-list>

    476个PyTorch资源大合集推荐

- <https://github.com/zergtant/pytorch-handbook>

    pytorch handbook是一本开源的书籍

- <https://github.com/ShusenTang/Dive-into-DL-PyTorch>
  
    本项目将《动手学深度学习》（Dive into Deep Learning）原书中的MXNet代码实现改为PyTorch实现

    **Book**: <https://github.com/d2l-ai/d2l-zh> (MXNet)

    **PDF**: <https://github.com/OUCMachineLearning/OUCML/blob/master/BOOK/Dive-into-DL-PyTorch.pdf>

- <https://github.com/bentrevett/pytorch-seq2seq>

    Tutorials on implementing a few sequence-to-sequence (seq2seq) models with PyTorch and TorchText.


#### Tool & Library

- <https://github.com/microsoft/tensorwatch>

    ```shell
    conda install pytorch-nightly -c pytorch
    conda install graphviz
    conda install torchvision
    conda install tensorwatch
    ```
    ```python
    import tensorwatch as tw
    tw.draw_model(model, [1, 3, 224, 224])   # 参数2-input_shape 参数3-orientation，'LR'或'TB'，表示左右或上下布局
    tw.model_stats(model, [1, 3, 224, 224])  # 网络参数统计
    ```
    ![](https://raw.githubusercontent.com/liuyaox/ImageHosting/master/for_markdown/tensorwatch_draw_model.png)

    ![](https://raw.githubusercontent.com/liuyaox/ImageHosting/master/for_markdown/tensorwatch_model_stats.png)

- <https://github.com/lanpa/tensorboardX>

    tensorboard for pytorch (and chainer, mxnet, numpy, ...)

    **Article**: [PyTorch 深度学习训练可视化工具 tensorboardX - 2020](https://mp.weixin.qq.com/s?__biz=MzIwOTc2MTUyMg==&mid=2247495343&idx=3&sn=cba2b5d710ed8bfe8b3247468483bdd7)

- <https://github.com/sksq96/pytorch-summary>

    Model summary in PyTorch similar to `model.summary()` in Keras

- <https://github.com/lyken17/pytorch-opcounter>

    Count the FLOPs of your PyTorch model,  能够统计PyTorch模型的参数个数和计算量FLOPS(每秒浮点运算次数Floating-point operations per second)

- <https://github.com/BlackHC/TfPyTh>

    切换TensorFlow与PyTorch   Putting TensorFlow back in PyTorch, back in TensorFlow (differentiable TensorFlow PyTorch adapters).

- 【Great】[pytorch实用工具总结 - 2018](https://zhuanlan.zhihu.com/p/33992733)


#### Article

- [PyTorch internals - 2019](http://blog.ezyang.com/2019/05/pytorch-internals/)

    **Chinese**: [PyTorch内部机制，来自核心开发者的全面解读](https://www.jiqizhixin.com/articles/2019-06-02-4)

- [一文弄懂Pytorch的DataLoader, DataSet, Sampler之间的关系 - 2019](https://zhuanlan.zhihu.com/p/76893455)

- [PYTORCH VS. TENSORFLOW: WHICH FRAMEWORK IS BEST FOR YOUR DEEP LEARNING PROJECT? - 2019](https://builtin.com/data-science/pytorch-vs-tensorflow)

    **Chinese**: [TensorFlow与PyTorch之争，哪个框架最适合深度学习](https://mp.weixin.qq.com/s?__biz=MzA3MzI4MjgzMw==&mid=2650769131&idx=2&sn=4def04d2834637e38915641190727b60)

- [Keras和PyTorch的视觉识别与迁移学习对比 - 2018](https://cloud.tencent.com/developer/article/1358228)

- [同一个模型用theano，tf，pytorch实现，performance可能差距较大吗](https://www.zhihu.com/question/268494717)


#### Practice

- <https://github.com/IgorSusmelj/pytorch-styleguide>

    A PyTorch Tools, best practices & Style guide


#### Book

- <https://github.com/deep-learning-with-pytorch/dlwpt-code>

    Deep Learning with PyTorch