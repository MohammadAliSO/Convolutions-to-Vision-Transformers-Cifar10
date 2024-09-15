# Convolutions-to-Vision-Transformers-Cifar10
Implementation of the concepts expressed in the article (CvT: Introducing Convolutions to Vision Transformers , Cifar10 DataSet )

## Abstract

We present in this paper a new architecture, named Convolutional vision Transformer (CvT), that improves Vision Transformer (ViT) in performance and efficiency by introducing convolutions into ViT to yield the best of both designs. This is accomplished through two primary modifications: a hierarchy of Transformers containing a new convolutional token embedding, and a convolutional Transformer block leveraging a convolutional projection. These changes introduce desirable properties of convolutional neural networks (CNNs) to the ViT architecture (i.e. shift, scale, and distortion invariance) while maintaining the merits of Transformers (i.e. dynamic attention, global context, and better generalization). We validate CvT by conducting extensive experiments, showing that this approach achieves state-of-the-art performance over other Vision Transformers and ResNets on ImageNet-1k, with fewer parameters and lower FLOPs. In addition, performance gains are maintained when pretrained on larger datasets (e.g. ImageNet-22k) and fine-tuned to downstream tasks. Pretrained on ImageNet-22k, our CvT-W24 obtains a top-1 accuracy of 87.7% on the ImageNet-1k val set.

![image](https://github.com/user-attachments/assets/362ef70f-5076-4f21-9428-c0173762435e)
The pipeline of the proposed CvT architecture.     
(a) Overall architecture, showing the hierarchical multi-stage structure facilitated by the Convolutional Token Embedding layer.     
(b) Details of the Convolutional Transformer Block, which contains the convolution projection as the first layer.      

![image](https://github.com/user-attachments/assets/eed0dcd6-fc9e-48fc-afbd-a948c654ae24)
(a) Linear projection in ViT.     
(b) Convolutional projection.     
(c) Squeezed convolutional projection. Unless otherwise stated, we use (c) Squeezed convolutional projection by default.      


We execute this code on Cifar10 Dataset and  train on 10 epoch get about 70% validation.

Download Dataset: https://www.cs.toronto.edu/~kriz/cifar.html      
Orginal Code git: https://github.com/microsoft/CvT      
CVT paper: https://arxiv.org/abs/2103.15808      


**Notice**:  this code test with python 3.9.13 and torch 1.7.1 (see on requirements.txt)		

```bash
python -m pip install -r requirements.txt
```



### Report

Dataset Cifar10 example

![image-20240916010511594](C:\Users\MohammadAli\AppData\Roaming\Typora\typora-user-images\image-20240916010511594.png)



Result train 

```
Epoch1/10
Epoch [0], train_loss: 1.6958, val_loss: 1.4269, val_acc: 0.4648
Epoch2/10
Epoch [1], train_loss: 1.3566, val_loss: 1.2685, val_acc: 0.5273
Epoch3/10
Epoch [2], train_loss: 1.2043, val_loss: 1.1400, val_acc: 0.5977
Epoch4/10
Epoch [3], train_loss: 1.0940, val_loss: 1.1478, val_acc: 0.5664
Epoch5/10
Epoch [4], train_loss: 0.9759, val_loss: 0.9823, val_acc: 0.6289
Epoch6/10
Epoch [5], train_loss: 0.8778, val_loss: 0.9891, val_acc: 0.6523
Epoch7/10
Epoch [6], train_loss: 0.7948, val_loss: 1.0040, val_acc: 0.6875
Epoch8/10
Epoch [7], train_loss: 0.6974, val_loss: 0.9673, val_acc: 0.6719
Epoch9/10
Epoch [8], train_loss: 0.6242, val_loss: 1.0202, val_acc: 0.6367
Epoch10/10
Epoch [9], train_loss: 0.5507, val_loss: 0.9920, val_acc: 0.6680
```

![image-20240916010621902](C:\Users\MohammadAli\AppData\Roaming\Typora\typora-user-images\image-20240916010621902.png)