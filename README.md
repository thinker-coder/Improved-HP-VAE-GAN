Python implementation code for the paper titled,

Title: Data augmentation in material images using the improved HP-VAE-GAN

Authors: Yuexing Han1, 2, 3, Yuhong Liu1, Qiaochuan Chen1, *

1 School of Computer Engineering and Science, Shanghai University, Shanghai, 200444, China

2 Key Laboratory of Silicate Cultural Relics Conservation (Shanghai University), Ministry of Education, Shanghai, 200444, China

3 Zhejiang Laboratory, Hangzhou, 311100, China

# Improved-HP-VAE-GAN

1.Requirements

PyTorch-gpu == 1.7.0

Software development environment should be any Python integrated development environment used on an NVIDIA video card.

Programming language: Python 3.8.

2.Usage

For training a single image, use the following command for example:

CUDA_VISIBLE_DEVICES=0 python train_image.py --image-path data/imgs/real_alloy_images/13-00.jpg --vae-levels 3 --niter 5000 --checkname myimagetest --visualize

Use eval_image.py to generate samples from an "experiment" folder created during training. For example, the following line will generate 100 image samples:

CUDA_VISIBLE_DEVICES=0 python eval_image.py --num-samples 100 --exp-dir run/1/myimagetest/experiment_0

In order to extract images, use the extract_images.py files similarly:

CUDA_VISIBLE_DEVICES=0 python extract_images.py --max-samples 100 --exp-dir run/1/myimagetest/experiment_0/eval
