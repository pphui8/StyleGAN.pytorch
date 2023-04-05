```bash
# train
python train.py --config configs/sample.yaml

# generate
python generate_samples.py --generator_file /root/autodl-tmp/checkpoints/StyleGAN.pytorch/asian_stars/models/GAN_GEN_SHADOW_5_160.pth --num_samples 10 --output_dir /sample --config ./configs/asain_256.yaml

## generate grid
python generate_grid.py --generator_file /root/autodl-tmp/checkpoints/StyleGAN.pytorch/asian_stars/models/GAN_GEN_SHADOW_6_1.pth --output_dir /sample

# zip
zip -r sample.zip ./sample
```
