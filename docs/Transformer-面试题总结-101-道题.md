# Transformer 面试题总结 101 道题

> 来源：[`xqkxndvkg5.feishu.cn/docx/UjhEdxfSgoyf81xlbbrc0ygXnsb`](https://xqkxndvkg5.feishu.cn/docx/UjhEdxfSgoyf81xlbbrc0ygXnsb)

1，请阐述 Transformer 能够进行训练来表达和生成信息背后的数学假设，什么数学模型

或者公式支持了 Transformer 模型的训练目标？请展示至少一个相关数学公式的具体推

导过程。

2，Transformer 中的可训练 Queries、Keys 和 Values 矩阵从哪儿来？Transformer 中为

何会有 Queries、Keys 和 Values 矩阵，只设置 Values 矩阵本身来求 Attention 不是更简

单吗？

3，Transformer 的 Feed Forward 层在训练的时候到底在训练什么？

4，请具体分析 Transformer 的 Embeddigns 层、Attention 层和 Feedforward 层的复杂度

5，Transformer 的 Positional Encoding 是如何表达相对位置关系的，位置信息在不同的

Encoder 的之间传递会丢失吗？

6，Transformer 中的 Layer Normalization 蕴含的神经网络的假设是什么？为何使用

Layer Norm 而不是 Batch Norm？Transformer 是否有其它更好的 Normalization 的实现

？

独立同分布假设

7，Transformer 中的神经网络为何能够很好的表示信息？

8，请从数据的角度分析 Transformer 中的 Decoder 和 Encoder 的依存关系

9，请描述 Transformer 中的 Tokenization 的数学原理、运行流程、问题及具体改进方法

10，请描述一下你认为的把 self-attention 复杂度从 O(n2) 降低到 O(n)有效方案.

11，Bert 的 CLS 能够有效的表达 Sentence Embeddings 吗？

12，使用 BPE (Byte-Pair Encoding) 进行 Tokenization 对于 Cross-lingual 语言模型的意义

是什么？是否会有问题及如何改进？

13，如果使用 Transformer 对不同类别的数据进行训练，数据集有些类别的数据量很大

(例如有 10 亿条)，而大多数类别的数据量特别小(例如可能只有 100 条)，此时如何训练

出一个相对理想的 Transformer 模型来对处理不同类别的任务？

14，如何使用使用多种类小样本对 Transformer 训练而取得很好的分类效果，请详述背

后的架构设计和数学机制

15，在给 Transformer 输入 Embeddings 的时候是否可以使用多方来源的词嵌入训练模

型？请阐述背后的数学原理及工程上的具体实现机制

16，更深更宽的 Transformer 网络是否意味着能够获得更强的预训练模型？请至少从 3

个角度，例如架构的工程化落地、参数的信息表达能力、训练任务等，来展开具体的分析

17，如何大规模降低 Transformer 中 Embedding 中的参数数量？请至少具体分析一种具

体方法背后的数学原理和工程实践

18，请描述 Trasnformer 不同的 Layer 之间的 FeedForward 神经网络之间的联系，例如

在 Bert 中不同 Layer 之间的 CLS 有什么关系、对角矩阵随着 Layer 的加深有何变化等

19，如何降低 Transformer 的 Feedforward 层的参数数量？请详述背后的数学原理和工

程实践

20，Transformer 的 Layer 深度过深，例如 512 个 Layer，会可能导致什么现象？请详述

背后的数学机制 21，Bert 中 NSP 可能的问题有些哪些？这些问题背后的数学原理是什么？如何改进？可

以去掉 NSP 训练任务吗？

22，请详解分析 Transformer 的 Batch 大小与训练的信息困惑度 ppl 的关系并阐明背后

的数学原理

23，请从数据的角度分析一下为何在对 Transformer 进行参数的 Quantization 的时候工

业界最终选择了 INT8？包括压缩的具体过程、KL 散度、长尾分布等。如何处理

Quantization 后模型质量降低度情况？

24，以 Transformer 为代表的的 Neuron Network 逐渐主导了人工智能各领域，例如

NLP, CV 等的信息表示。请从数学的角度阐述为什么 Neuron Network 能够代表任意人复

杂度的信息？使用神经网络表达信息具体有什么优势？

25，请描述至少三种判断 Transformer 中神经元 Neuron 相对重要程度的具体方法及其背

后的数学原理

26，为什么说 Transformer 的注意力机制是相对廉价的？注意力机制相对更对于 RNN 系

列及 Convolution 系列算法而言在计算上（尤其是计算复杂度）有什么优势？

27，请用具体例子阐述使用 Multi-head 的物理机制和并从数学的视角来推导其有效性的

原因

28，请分享一下至少三种提升 Transformer 预测速度的具体的方法及其数学原理

29，请分别描述 Bert 的 MLM 和 NSP 技术(例如 Sampling) 的问题及具体改进方式

30，请阐述使用 Transformer 实现 Zero-shot Learning 数学原理和具体实现流程

31，请至少描述 2 种对来自不同训练模型训练出来的 Embeddings 进行相似度比较的方

法的具体实现

32，如何使得一个小模型，例如 LSTM，具有一个大模型，例如 Bert 的能力？

33，为何训练后的 BERT 模型不能够很容易的实现模型泛化？请从架构机制和数学原理

部分进行分析

34，GPT 的 auto-regressive 语言模型架构在信息表示方面有什么架构上的缺陷？

35，请描述 BERT 中 MLM 实现中的至少 5 个缺陷及可能的解决方案

36，请从数学的角度阐明如何实现对 Transformer 任意位置和长度进行 Mask 的具体实现

方式

37，请描述 Encoder 和 Decoder 中 Attention 机制的三点不同之处并阐述其数学原理

38，请描述 Transformer 中 Decoder 的 Embedding layers 架构设计、运行流程和数学原

理 39，请描述 Transformer 进行 Training 的全生命周期的在 Decoder 中是如何进行

Embedding 的呢？请阐述其流程和数学原理

40，请描述 Transformer 进行 Inference 的全生命周期的在 Decoder 中是如何进行

Embedding 的呢？请阐述其流程和数学原理

41，Transformer 如果采用和 Inference 同样的流程来进行 Training，会有什么问题？请

至少指出 3 点问题并说明背后的数学原理

42，为何 Transformer 的 Matrix Dimensions 是 3D 的？请详述每个 Dimension 大小的改

变是如何影响整个 Transformer 训练过程的？请详述其具体的流程和数学原理

43，请描述只由一个 Encoder 和 Decoder 的 Transformer 使用了 Attention 的三个地方及

其功能

44，请分别描述当进行 Training 和 Inference 的时候 Masking 在 Transformer 三大不同

类型使用 Attention 机制的地方的具体功能和数学实现

45，请描述 Transformer 的 Training Loss 具体工作流程和背后的数学公式

46，请阐述 Multi-head Attention 机制中通过 Linear layer 的 Matrices 计算 Query、Key

、Value 时候进行 logical partition 和 physical partition 的异同及背后的数学原理

47，请阐述 Transformer 中所有能够 trainable 的操作及其功能

48，请阐述 Query、Key、Value 在 Transformer 中具体的功能

49，为什么 Transformer 中的 Attention Score 能够衡量不同 Words 之间 Relevance 的不

同程序呢？请说明背后的物理机制和数学原理

50，Transformer 是如何知道什么样的 Weights 能够使得其更好的表达不同信息部分的不

同程度的注意力的？请描述其运行机制和背后的数学假设

51，如何减少 Transformer 中训练后的 Word Embeddings 的 Bias？请阐述其背后的数学

原理和实现流程

52，如何解决 Self-attention 和 Word 和自己的 Attention 最大的问题？

53，为什么 Transformer 能够对 NLP、CV 等任何 AI 领域的信息进行有效表示？

54，为何通过 Ground Truth 就能够训练 Transformer 使其具有泛化能力?

55，为什么在 Transformer 的 Attention 计算的时候需要进行 Scaling 操作，请从神经网

络和数学原理的角度进行解释

56，在 Transformer 中，一个输入文本词汇的顺序是由 position encoding 来表达还是由

multi-head attention 来具体实现的？请阐述运行机制和数学原理

57，请描述 multi-head attention 的至少三种实现方式并提供相应的示例实现代码 58，请描述 Transformer 中三种类型的 non-linear 操作并阐述请数学原理

59，相比于 RNN 等，为何 Transformer 论文作者声称“Attention is all you need”？请重点

从数学的角度阐述其原因

60，请具体谈一下 Teacher forcing 的数学原理及其在 Transformer 中的至少两个地方的

应用

61，在 Transformer 的架构中 Decoder 在进行 Inferencer 的时候同时接收来自 Encoder

和 Decoder 的输入信息，以 NLP 为例，这两种类型的输入在词法、语法、语义上是否有

所不同？背后的数学原理是是什么？

62，请描述 BERT 的 Tokenization 机制的优势和不足，及针对不足的解决方案

63，Transformer 的 Input 长度为何受限？请阐明数学原因并提供至少一种可能的解决方

案

64，如果使用 Pytorch 实现 Transformer，如何巧妙的使用或者停用

optimizer.zero_grad()来训练大模型，例如内存只允许一次只能训练一个 Instance？

65，训练 Transformer 时候，如果因为内存大小限制导致连一个 Instance 的训练都无法

容纳，该如何完成所有 Instance 的训练，请描述详细的工程过程

66，请从 Data Science 的角度分析为何 Transformer 是目前最 generic 的 AI 模型？

67，请分析一下是什么能够从根本上限制 Transformer 的能力？

68，请描述 Transformer 训练时候的 Label Smoothing 核心功能、运行机制和数学原理

69，请描述 Beam Search 算法在 Transformer 中的具体应用并阐述其有效性的数学数学

假设和数学公式

70，请分析如何使用 Transformer 来有效的对 Knowledge Graph 中的 Edge 进行

Encoding？

71，如何由你使用 Transformer 来实现一个对话系统，如何判定用户当前的交流的内容

是否离题，例如在办理一项业务过程中突然对话机器人今天天气怎么？请阐述架构思路及

数学原理

72，请使用 Einsum 的方式编码实现 Transformer 的 Attention 机制

73，请描述 Transformer 使用动态 Batch Size 进行训练的原理、流程和数学证明

74，如何使用 Transformer 实现一个能够同时预测 Intent 和 Entity 的信息系统？

75，使用一个 Transformer 模型同时预测 Intent 和 Entity 有什么弊端？请分析该弊端的

产生的原因并提出具体的解决方案 76，使用 Transformer 实现 NLU 的时候需要使用 Masking 机制吗？请解释工程原因及数

学原理

77，如何使用 Transformer 来描述多轮对话？请描述工程架构和数学原理

78，请问使用 Transformer 和 CRF 做 NER 哪个更好？请提出至少 3 个工程落地的最佳实

践。

79，请问使用手动实现 Transformer 和使用 BERT 哪个做 Intent 识别效果更好？请阐述

具体的原因和工程实践过程

80，为何 Transformer 比 RNN、LSTM 等传统神经网络具有更高性价比且能够更有效的

使用内存和计算资源？

81，Transformer 为何只使用 Attention 机制就解决了 CNN、LSTM、RNN 等能解决的一

切问题及这些传统网络解决不了的问题？

82，当有新的数据的来训练 Transformer 模型的时候，如何如何实现模型的增量训练？

83，请分析如何使用 Transformer 探测 Toxic 语言，Toxic 语言能够通过 Tansformer 移

除吗？请分析工程实践和数学原理

84，Transformer 在通用语言领域(例如，整个英语语言领域)能否实现 Word Analogy 功

能，请分析具体的工程原因和数学原因

85，如何分类语料库中的有些 Label 标注是错误的，如何使用 Transformer 来发现分类

语料库中的 Bad Label？请描述具体的工程过程

86，为何说 Transformer 是一种理想的 Bayesian 模型实现？请阐述数学原理及具体的场

景案例

87，请描述 Transformer 至少三个使用 Bayesian 具体地方并阐述在这些具体地方使用

Bayesian 的数学原理

88，为什么说 Transformer 基于对 Bayesian 的时候极大的降级了训练时候的 overfitting

？请阐述工程工程和数学原理

89, 请详解描述使用 Transformer 进行 Transfer Learning 中具体 Prior 和 Posterior

Probability 地方及其具体的功能和数学原理

90, 请描述 Transformer 在 Training 和 Inference 对 MLE(maximum likelihood estimation)

模型具体应用

91, 请描述 Transformer 在 Training 的时候具体使用 MAP(Maximum A Posteriori)

estimation 模型的地方并描述其流程机制和数学原理

92, 请描述 Transformer 在训练的过程中什么情况下使用 MLE 和 MAP 是基本没有区别的

，其背后的数学原理是什么？93, 为什么一般情况下 Transformer 的训练不会完全使用 Bayesian 模型而是更倾向于采用

Naive Bayes？请具体阐述其架构和背后的数学原理

94，请从 Bayesian 模型的角度分析 Transformer 中代表模型例如 GPT3 为何是模型越宽

越深越好？

95，请描述 Naive Bayes 在 Transformer 的 Auto-encoding 模型训练时候的具体应用及其

有效性的数学证明

96，请描述 Naive Bayes 在 Transformer 的 Auto-regressive 模型训练时候的具体应用，

这样能够在小样本数据的时候帮助取得优质德训练效果？其有效性的数学证明是什么？

97，请描述 Naive Bayes 在 Transformer 的 Generative Process 的具体流程和有效性的数

学证明

98，使用 Naive Bayes 来完成 Transformer 的 Generative Process 会有什么问题？问题背

后工程实现限制和数学原因是什么？

99，如何使用 Transformer 和 LDA 结合完成信息的多分类模型？请实现示例代码

100，为何说 Transformer 是目前人工智能领域工程落地实践 Bayesian 理论的典型？请

从数学的的角度进行完整的证明（至少包含 Encoder-Decoder、Training、Inference 等对

Bayesian Theory 的具体实现）

101，在 Gavin 看来，“Transformer 赋予机器思想。Transformer 是实现多模态目前最佳

的底层引擎，是人工智能、贝叶斯理论、认知模型演进的统一架构，是学术界（无意间）

基于 Bayesian 理论通过神经网络实现的（计算机）认知模型持续的 Evolving 的理想架构

体系”，你怎么看？