# ESRPCB

### V1.0, April 16th, 2025

**Authors:** [Xiem HoangVan](https://sites.google.com/site/xiemhoang/), [Thanh Nguyen Canh](https://thanhnguyencanh.github.io/), Dang Bui Dinh, Van-Truong Nguyen 


This is an official implementation for "ESRPCB: an Edge guided Super - Resolution model and Ensemble learning for tiny Printed Circuit Board Defect detection".

# 1. License


If you use IRAF-SLAM in an academic work, please cite:
  
    @article{thanhnc_ESRPCB,
      title={ESRPCB: an Edge guided Super - Resolution model and Ensemble learning for tiny Printed Circuit Board Defect detection},
      author={Xiem Hoang Van, Thanh Nguyen Canh, Dang Bui Dinh, Van-Truong Nguyen},
      journal={}, 
      volume={},
      number={},
      pages={},
      year={2025}
     }


## 2. Create Environment
### 2.1. Install the environment
Make Conda Environment
```
conda env create -f setup.txt
conda activate pcb
```
Note: If you want to rename the new environment, edit the [`setup.txt`](setup.txt) file by changing the first line:
```
name: <new environment name>
```

## 3. Dataset
### 3.1 Super-resolution Dataset
If you want to retrain the ESRPCB model, please download the pcb super-resolution dataset from [Google Drive](https://drive.google.com/file/d/10EWL9DhGOONFnoOL8ZYB19iRbCH0Vlgy/view?usp=sharing)

The structure of the dataset will be like this:
```
dataset/
    sr-dataset/
        train/
            HR/
            LR/
        test/
            HR/
            LR/

```
### 3.2 PCB Defect Dataset
If you want to retrain defect detection model, please download the pcb dataset from [Kaggle](https://www.kaggle.com/datasets/norbertelter/pcb-defect-dataset)

The structure of the dataset will be like this:
```
dataset/
    pcbdefect/
        train/
            images/
            labels/
        val/
            images/
            labels/
        test/
            images/
            labels/

```

## 4. Training
To train the ESRPCB model, use the file [train_esrpcb.ipynb](train_esrpcb.ipynb).

To train the YOLOv8 and YOLOv9 model, use the file [train_yolo.ipynb](train_yolo.ipynb).
