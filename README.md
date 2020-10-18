# Learningnote
## Network Compression

- Network Puring：在训练完了一个network后，对不重要的weight和neural删除，然后重新训练，修补影响；之所以要先训练好后再来删除weigh是因为前期neural小的话会非常难训练出结果

- Knowledge Distillation：利用一个已经学好的model，来教小model如何做好任务，在大model学完了之后，让小model根据输入的参数和大model的输出结果来进行训练；有个问题 为什么不直接用小model来训练呢，这是因为直接用小model来进行训练是很训练出想要的结果 ，通常只用在Classification，而且学生只能从头学起

- Architecture Design：利用更少的参数来达到原本的layer的效果，这是因为有些layer本身参数就很冗，例如DNN；一般用新的layer来模拟旧的layer

- Parameter Quantization：将NN常用的计算单位float32/float64压缩成更小的单位，已办对已经训练好的moedel使用，比如有的时候对系统来说参数为1,2,3 的意义是一样的，80，81,82的意义是一样的，这种情况下可以直接对其进行分类，缩小单位
