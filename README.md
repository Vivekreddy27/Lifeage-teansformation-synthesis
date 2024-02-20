# Lifeage-transformation-synthesis

## Pre-Requisits
You must have a **GPU with CUDA support** in order to run the code.

This code requires **PyTorch** and **torchvision** to be installed, please go to [PyTorch.org](https://pytorch.org/) for installation info.<br>
We tested our code on PyTorch 1.4.0 and torchvision 0.5.0, but the code should run on any PyTorch version above 1.0.0, and any torchvision version above 0.4.0.

The following python packages should also be installed:
1. opencv-python
2. visdom
3. dominate
4. numpy
5. scipy
6. pillow
7. unidecode
8. requests
9. tqdm
10. dlib

If any of these packages are not installed on your computer, you can install them using the supplied `requirements.txt` file:<br>
```pip install -r requirements.txt```

## Training/Testing on FFHQ-Aging
1. Download the FFHQ-Aging dataset. Go to the [FFHQ-Aging dataset repo](https://github.com/royorel/FFHQ-Aging-Dataset) and follow the instructions to download the data.

2. Prune & organize the raw FFHQ-Aging dataset into age classes:
```
cd datasets
python create_dataset.py --folder <path to raw FFHQ-Aging directory> --labels_file <path to raw FFHQ-Aging labels csv file> [--train_split] [num of training images (default=69000)]
```
