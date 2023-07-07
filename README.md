## Deep-learning-generated-Xe-DECT-ventilation-images

This repository is an implementation of "Generating Ventilation Images from Virtual Non-Contrast Xenon-Enhanced Dual-Energy CT using Multitasking Conditional Generative Adversarial Networks."

<p align="center"><img width="100%" src="/Figures/multitasking conditional GAN architecture.png" /></p>

## Requirements
- tensorflow 1.13.1
- numpy 1.15.2
- opencv 4.1.0.25
- matplotlib 2.2.3
- pickleshare 0.7.4
- simpleitk 1.2.0
- scipy 1.1.0

## Deep learning-generated Xe-DECT ventilation images Results

### Running the Code

1. Please contact us to download the VGG16 weights (previously downloadable from [here](https://github.com/ChengBinJin/MRI-to-CT-DCNN-TensorFlow)).

2. Download trained model from [here](https://gitlab.com/fumin.guo/dante_capaldi_DLMRI).

3. Save the VGG16 weights file (caffe_layers_value.pickle) to ./Models_zoo/

4. Save the contents from the trained model to ./model/DLVentMRI/20200815-2145/model4/

5. We provided an example image for test: 014.png (left and right panels: specific ventilation map and mask)

6. Run >> python run_prediction.py --load_model=20200815-2145 --dataset=DLVentMRI --test_filename=./input/014.png

7. The results are save as ./test/DLVentMRI/20200815-2145/model4/000.png
