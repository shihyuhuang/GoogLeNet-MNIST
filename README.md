# GoogLeNet_MNIST
![截圖 2021-08-22 13 35 54](https://user-images.githubusercontent.com/61773397/130344044-219a25b9-890b-4568-b951-8e59bb60e546.png)
1.	GoogLeNet 的 Inception V1架構在 ILSVRC-2014 比賽中的分辨項目獲得第一名，Top-5 Error=6.67%。GoogLeNet同時將不同大小的 Kernel 的 Convolution 連同 Max-pooling，Concatenate 輸出成 Output，這整個為 Inception 模組，也使用了 Bottleneck 的概念，加入 1x1 Convolution，藉由 1x1 Conv 大量減少參數。他大概使用了 6.8 百萬個參數，比 AlexNet 少九倍，更比 VGG-16 少二十倍，也就是說 GoogleNet 的模型更為輕巧，因此我將model改為GoogLeNet以提升Accuracy。

2.	在分類訓練中，最常使用的loss fun.為nn.CrossEntropyLoss()，這個loss fun.結合了nn.LogSoftmax() 和nn.NLLLoss()這兩個函數，因此我將loss fun. 改為使用nn.CrossEntropyLoss()。

3.	其他的部分沒有改變，而error從原本的95%提升到99%。
