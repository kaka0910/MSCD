# MSCD
Dataset and code release for "A Multi-Spectral Change Detection Dataset (MSCD) using Sentinel-2 satellite imagery". Visualization of MSCD samples with RGB images, single infrared band images and binary change detection masks are as shown as :

<img width="750" alt="image" src="https://github.com/kaka0910/MSCD/blob/main/Figs/dlcv_dataset.jpg">

**Abstract**: Change detection is a key research topic in the field of remote sensing image analysis. It aims to identify changes on the Earth's surface by comparing images captured at different times over the same geographic area. However, change detection based on visible light images is often susceptible to illumination variations, which can significantly degrade performance. To address this limitation, we construct a Multi-Spectral Change Detection Dataset (MSCD) using Sentinel-2 satellite imagery and provide benchmark results using several deep learning methods. Furthermore, it is feasible to evaluate the effectiveness of incorporating infrared bands by proposing an improved network based on STANet tailored for multi-spectral change detection. Experimental results demonstrate that multi-spectral fusion methods significantly outperform those using only visible or infrared bands individually, highlighting the advantages of multi-spectral data for change detection tasks and offering a reliable solution for analyzing surface changes in complex scenarios.

### Install
Base Environment: RTX single 4090, CUDA==12.1, Python==3.8
- pip install torch==2.1.0 torchvision==0.16.0 torchaudio==2.1.0 
- pip install mmcv==2.1.0 -f
- See `requirements.txt` for other installation.

### MSCD dataset structure
```
MSCD Dataset
  |--train     # Training dataset，训练集
     |--A      # Before dataset，变化前数据集
     |--B      # After dataset，变化后数据集
     |--label  # label，二值标签
  |--val       # Validation dataset，验证集
  |--test      # Test dataset，测试集，可以和验证集一样
```

### Usage
- Prepare MSCD Dataset. For details on how the data is loaded, please refer to the `opencd/datasets/mscd.py` file.
- Training: `python tools/train.py configs/stanet/stanet_base_256x256_40k_mscd.py --work-dir ./workspace/stanet_base_256x256_40k_mscd`
- Test: `python tools/test.py configs/changer/stanet_base_256x256_40k_mscd.py ./workspace/stanet_base_256x256_40k_mscd/best.pth --show-dir tmp_infer`


### Acknowledgment and connection
Thanks for your attention! This work is conducted based on the [OpenCD](https://github.com/likyoo/open-cd) project. We sincerely appreciate its well-designed framework and meticulous code implementation. If you would like to access the full dataset or have any suggestions, please leave a comment or contact the author directly.
