# Raphael-style-transfer

## Abstract

We use related methods based on convolutional neural networks to achieve style transfer.

The network that realizes style transfer is unified in a unified framework based on generator (endoer-decoder)-discriminator, and based on the unified architecture, the methods in some classic papers are implemented and used in Raphael's style transfer.

For the most basic **Gatys method**, we use a more efficient generator based on a fully-convolution-network fully-convolution-network instead of the original method to speed up the training process of style transfer. And implemented and explored the offline (off-line) and online (on-line) methods respectively. And based on the idea of cycle consistency in **CycleGAN**, an inverse generator is added to the Gatys method.

In view of the characteristics of Raphael's paintings, fine structures are used to support higher resolution, and image processing methods such as grayscale and edge enhancement are used as preprocessing processes to enhance the style transfer effect.

Under the same architecture, adding a module which is designed for style control between encoder and decoderr can realize **arbitrary style transfer**. The key to arbitrary style transfertransfer lies in the understanding of the information stored in the image style. The different understandings leads to two different representative methods, that is, **SwapStyle** and **AdaIN**. Under a unified framework, the two methods are compared to enhance the understanding of image style information.

## Files

* \net: codes of neural networks
* \old: the old codes
* transfer.py: codes of the off-line Gatys method 
* end2end_transfer.py: codes of the on-line Gatys method 
* cycle.py:  introducing cycle consistency in Gatys method
* StyleSwap.py: arbitrary style transfer with StyleSwap
* adain.py: arbitrary style transfer with AdaIN

## 摘要

使用基于卷积神经网络的相关方法实现风格迁移

将实现风格迁移的网络统一在基于generator(endoer-decoder) - discriminator的统一框架内，并且基于统一的架构，实现了一些经典论文中的方法，用于Raphael的风格迁移之中。

对于最基础的Gatys method，使用更高效的基于全卷积神经网络fully-convolution-network的generator替代原方法，加速风格迁移的训练过程。并且分别实现并探究了离线（off-line)和在线（on-line）的方法。并且基于CycleGAN中的循环一致的思想，为Gatys method添加逆向网络（inverse generator）。

针对Raphael画作的特点，使用精细的结构以支持更高的分辨率，并且使用灰度化、边缘增强等图像处理手段作为预处理过程增强风格迁移效果。

在相同的架构下，在encode和decoder之间加入控制风格的模块，可以实现任意风格迁移。任意风格迁移的关键，在于对储存图像风格的信息的理解。对其理解不同，也即SwapStyle和AdaIN两种不同的，任意风格迁移的方法。在统一的架构下，对比两种方法，旨在增强对图像风格信息的理解。


## 文件说明

* \net 定义网络模型
* \old 旧有代码，包括正则化探索，边缘提取增强等探索，使用PatchGAN的探索，以及用卷积作鉴定的部分尝试，一些旧有代码中运用的辅助函数等
* transfer.py off-line的Gatys风格迁移方法
* end2end_transfer.py on-line的Gatys风格迁移方法，在线方法也即端到端的训练方法
* cycle.py 在Gatys方法中加入逆向网络支持循环一致
* StyleSwap.py 任意风格迁移
* adain.py AdaIN任意风格迁移


