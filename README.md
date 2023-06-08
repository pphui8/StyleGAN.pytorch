# StyleGAN.pytorch

## checkpoints
链接: https://pan.baidu.com/s/1g1MU_p6tXqdKs_pomQfGPw  
提取码: e88f 复制这段内容后打开百度网盘手机App，操作更方便哦


## Features

- [x] Progressive Growing Training
- [x] Exponential Moving Average
- [x] Equalized Learning Rate
- [x] PixelNorm Layer
- [x] Minibatch Standard Deviation Layer
- [x] Style Mixing Regularization
- [x] Truncation Trick   
- [x] Using official tensorflow pretrained weights 
- [x] Gradient Clipping
- [ ] Multi-GPU Training
- [ ] FP-16 Support
- [ ] Conditional GAN

## How to use

### Requirements
- yacs
- tqdm
- numpy
- torch
- torchvision
- tensorflow(Optional, for ./convert.py)

### Running the training script:
Train from scratch:
```shell script
python train.py --config configs/sample.yaml
```

### Using trained model:
Resume training from a checkpoint (start form 128x128):
```shell script
python train.py --config config/sample.yaml --start_depth 5 --generator_file [] [--gen_shadow_file] --discriminator_file [] --gen_optim_file [] --dis_optim_file []
```
### Style Mixing

```shell script
python generate_mixing_figure.py --config config/sample.yaml --generator_file [] 
```

<p align="center">
     <img src=diagrams/figure03-style-mixing-mix.png width=90% /> <br>
</p>

> Thanks to dataset provider:Copyright(c) 2018, seeprettyface.com, BUPT_GWY contributes the dataset.

### Truncation trick

```shell script
python generate_truncation_figure.py --config configs/sample_cari2_128_truncation.yaml --generator_file cari2_128_truncation_gen.pth
```

<p align="center">
     <img src=diagrams/figure08-truncation-trick.png width=90% /> <br>
</p>

### Convert from official format
```shell script
python convert.py --config configs/sample_ffhq_1024.yaml --input_file PATH/karras2019stylegan-ffhq-1024x1024.pkl --output_file ffhq_1024_gen.pth
```

## Reference

- **stylegan[official]**: https://github.com/NVlabs/stylegan
- **pro_gan_pytorch**: https://github.com/akanimax/pro_gan_pytorch
- **pytorch_style_gan**: https://github.com/lernapparat/lernapparat

## Thanks

Please feel free to open PRs / issues / suggestions here.

## Due Credit
This code heavily uses NVIDIA's original 
[StyleGAN](https://github.com/NVlabs/stylegan) code. We accredit and acknowledge their work here. The 
[Original License](/LICENSE_ORIGINAL.txt) 
is located in the base directory (file named `LICENSE_ORIGINAL.txt`).
