# DRRN-pytorch
This is an unoffical implementation of "Deep Recursive Residual Network for Super Resolution (DRRN)" , CVPR 2017 in Pytorch. [[Paper]](http://cvlab.cse.msu.edu/pdfs/Tai_Yang_Liu_CVPR2017.pdf) 

You can also get the offical implementation [here](https://github.com/tyshiwo/DRRN_CVPR17).

The DRRN implementation is modified from the implementation of [VDSR](https://cv.snu.ac.kr/research/VDSR/) by [@Jiu XU](https://github.com/twtygqyy/pytorch-vdsr).

## Usage
### Training
```
usage: main.py [-h] [--batchSize BATCHSIZE] [--nEpochs NEPOCHS] [--lr LR]
               [--step STEP] [--cuda] [--resume RESUME]
               [--start-epoch START_EPOCH] [--clip CLIP] [--threads THREADS]
               [--momentum MOMENTUM] [--weight-decay WEIGHT_DECAY]
               [--pretrained PRETRAINED]
               
optional arguments:
  -h, --help            Show this help message and exit
  --batchSize           Training batch size
  --nEpochs             Number of epochs to train for
  --lr                  Learning rate. Default=0.1
  --step                Learning rate decay, Default: n=10 epochs
  --cuda                Use cuda?
  --resume              Path to checkpoint
  --clip                Clipping Gradients. Default=0.4
  --threads             Number of threads for data loader to use Default=1
  --momentum            Momentum, Default: 0.9
  --weight-decay        Weight decay, Default: 1e-4
  --pretrained          Path to the pretrained model, used for weight initialization (default: none)
```

### Evaluation
```
usage: eval.py [-h] [--cuda] [--model MODEL] [--dataset DATASET]
               [--scale SCALE]

PyTorch DRRN Evaluation

optional arguments:
  -h, --help         show this help message and exit
  --cuda             use cuda?
  --model MODEL      model path
  --dataset DATASET  dataset name, Default: Set5
```
An example of training usage is shown as follows:
```
python eval.py --cuda
```
