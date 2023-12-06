## Prerequisites
- Python 3
- CPU or NVIDIA GPU + CUDA CuDNN
-This repository provides a PyTorch implementation of PDC-cycleGAN. Our model mainly makes modifications to the generator and loss function.

## Getting Started
### Installation
- Install torch == 1.10.0+cu113 (http://pytorch.org) and other dependencies (e.g., torchvision == 0.11.0+cu113).

### PDC-CycleGAN train/test
- To view training results and loss plots, run `python -m visdom.server` and click the URL http://localhost:8097.

- Train a model:
```bash
#!./scripts/train_cyclegan.sh
python train.py --dataroot ./datasets/maps --name maps_cyclegan --model cycle_gan
```
To see more intermediate results, check out `./checkpoints/maps_cyclegan/web/index.html`.
- Test the model:
```bash
#!./scripts/test_cyclegan.sh
python test.py --dataroot ./datasets/maps --name maps_cyclegan --model cycle_gan
```
- The test results will be saved to a html file here: `./results/maps_cyclegan/latest_test/index.html`.


