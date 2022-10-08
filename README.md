# TinySSD-Pytorch
AI Experiment Personal Homework

## :wrench: 依赖以及安装

- NVIDIA-SMI Version >= 517.8
- CUDA Version >= 11.7
- Python >= 3.8 (推荐使用[Anaconda](https://www.anaconda.com/download/#linux)或[Miniconda](https://docs.conda.io/en/latest/miniconda.html))
- [PyTorch >= 1.12.1](https://pytorch.org/)

#### 安装

1. 把项目克隆到本地

    ```bash
    git clone https://github.com/OliverGrace/TinySSD-Pytorch.git
    cd TinySSD-Pytorch-main
    ```

2. 安装依赖([Anaconda](https://www.anaconda.com/download/#linux)或pip)
    
    方式1：
    Anaconda 配置
    ```bash
    conda create --name TinySSD-Pytorch --file requirements_conda.txt
    ```
    
    方式2：
    pip 配置
    ```bash
    pip install -r requirements_pip.txt
    ```
3.  从[Release](https://github.com/OliverGrace/TinySSD-Pytorch/releases/tag/main)下载背景图片数据集并按照将数据放至data文件夹中，最终目录如下

    ```
    ├─data
      │  create_train.py
      │  
      ├─background
      │      000012-16347456122a06.jpg
      │	    ...
      │      191313-1519470793f344.jpg
      │      191328-15136820086f91.jpg
      │          
      ├─target
      │      0.jpg
      │      0.png
      │      1.png
      │      2.png
      │      
      └─test
             1.jpg
             2.jpg
    ```
    
4.  运行create_train.py生成训练集

    ```
    cd data
    python3 create_train.py
    ```
    运行完成后目录结构如下
    ```
    ├─data
      │  create_train.py
      │  
      ├─background
      │      000012-16347456122a06.jpg
      │	    ...
      │      191313-1519470793f344.jpg
      │      191328-15136820086f91.jpg
      │      
      ├─sysu_train
      │  │  label.csv
      │  │  
      │  └─images
      │          000012-16347456122a06.jpg
      │		...
      │          183201-15420187218258.jpg
      │          
      ├─target
      │      0.jpg
      │      0.png
      │      1.png
      │      2.png
      │      
      └─test
             1.jpg
             2.jpg
    ```
    
    
    
