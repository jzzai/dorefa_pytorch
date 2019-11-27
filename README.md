# Dorefa-net 
A pytorch implementation of [dorefa](https://arxiv.org/abs/1606.06160).The code is inspired by [LaVieEnRoseSMZ](https://github.com/LaVieEnRoseSMZ/AutoBNN) and [zzzxxxttt](https://github.com/kuangliu/pytorch-cifar).

## Requirements
* python > 3.5
* torch >= 1.1.0
* torchvision >= 0.4.0
* tb-nightly, future (for tensorboard)

## Cifar-10 Accuracy
Quantized model are trained from scratch

| Model        | W_bit   |  A_bit  |Acc  |
| :------ :  | :-----:  | :----:  |:----:  |
| resnet-18      | 32   |   32     | 94.71%     |
| resnet-18      |   4   |   4      |  94.05%     |
| resnet-18      |   ...   |   ...      |  ...     |


## Usages
* To train the model 
```
python3 cifar_train_eval.py
```
* To check the tensorboard log 
```
tensorboard --logdir='your_log_dir'
```
from the command line and then navigating to https://localhost:6006 should show the following.
....


## To do
- [ ]    Train on imagenet2012
- [ ]    Fold bn
- [ ]    Test speedup from quantization and bn fold
- [ ]    Deploy models to embedded devices
- [ ]    ...