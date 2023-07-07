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

## License

MIT License

Copyright (c) 2023 Sangyoon Lee

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
