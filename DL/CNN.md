```
w = nd.arange(24).reshape((3,2,2,2))
data = nd.arange(18).reshape((1,2,3,3))
b = nd.array([1, 2, 3])

out = nd.Convolution(data, w, b, kernel=w.shape[2:], num_filter=w.shape[0])
num_filter输出的channels/filter数目
kernel就是w的矩阵维度

data： (batch_size, channel, height, width)

batch_size: 样本个数
weight：(output_channels , in_channels, height, width)

in_channels与channel保持一致；原因是当data有多个channel时，需要相应个数的filter来对应每个channel（每个通道会有对应的权重）
```
