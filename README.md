## Deep-learning-generated-Xe-DECT-ventilation-images

This repository is the record of codes used in "Generating Ventilation Images from Virtual Non-Contrast Xenon-Enhanced Dual-Energy CT using Multitasking Conditional Generative Adversarial Networks." Codes for deep learning models and analyses can be found in other branches.

## Requirements
- torch 1.13.0
- torchvision 0.14.0
- numpy 1.21.5
- monai 1.2.dev2305
- matplotlib 3.1.1
- scipy 1.7.3
- statsmodels 0.10.1

## Deep learning-generated Xe-DECT ventilation images Results

### Preparing data

```
Structure format:
.datasets/train/
    [type of image]/
        [Patient number]/
            [Each DICOM slice of lung CT]

Example:
.datasets/train/
    inspiratory_CT/
        001/
            |--  001_0001_001.dcm
            |--  001_0001_002.dcm
            |--  001_0001_003.dcm
            |--  001_0001_004.dcm
                        .
                        .
                        .
        002/
            |--  002_0001_001.dcm
            |--  002_0001_002.dcm
            |--  002_0001_003.dcm
            |--  002_0001_004.dcm
                        .
                        .
                        .
    expiratory_CT
        001/
            |--  001_0002_001.dcm
            |--  001_0002_002.dcm
            |--  001_0002_003.dcm
            |--  001_0002_004.dcm
                        .
                        .
                        .
        002/
            |--  002_0002_001.dcm
            |--  002_0002_002.dcm
            |--  002_0002_003.dcm
            |--  002_0002_004.dcm
                        .
                        .
                        .
    emphysema_mask/
        001/
            |--  001_0003_001.dcm
            |--  001_0003_002.dcm
            |--  001_0003_003.dcm
            |--  001_0003_004.dcm
                        .
                        .
                        .
        002/
            |--  002_0003_001.dcm
            |--  002_0003_002.dcm
            |--  002_0003_003.dcm
            |--  002_0003_004.dcm
                        .
                        .
                        .
    ventilation_image/
        001/
            |--  001_0004_001.dcm
            |--  001_0004_002.dcm
            |--  001_0004_003.dcm
            |--  001_0004_004.dcm
                        .
                        .
                        .
        002/
            |--  002_0004_001.dcm
            |--  002_0004_002.dcm
            |--  002_0004_003.dcm
            |--  002_0004_004.dcm
                        .
                        .
                        .
.datasets/valid/

.datasets/test/
```
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
