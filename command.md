```bash
# train
python train.py --config configs/sample.yaml

# generate
python generate_samples.py --generator_file /data/pphui8/GAN_GEN_SHADOW_5_8.pth --num_samples 1000 --output_dir /sample

# zip
zip -r sample.zip ./sample
```
