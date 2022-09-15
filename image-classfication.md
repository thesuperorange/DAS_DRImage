# 14.3 Image Classification 


## Introduction

* 目標：透過有標記之眼底影像來偵測是否有糖尿病引發的視網膜病變
* 類別：分為五種嚴重程度
    - 0 - No DR
    - 1 - Mild
    - 2 - Moderate
    - 3 - Severe
    - 4 - Proliferative DR
* framework: Pytorch

## Data preparation
* From Kaggle:
    https://www.kaggle.com/c/diabetic-retinopathy-detection#description
* For training
    * Text data
        * train_img.csv / train_img_small.csv
        * train_label.csv/ train_label_small.csv
        * test_img.csv/ test_img_small.csv
        * test_label.csv/ test_label_small.csv
    * Image data
        * data/<#>_left.jpeg
        * data/<#>_right.jpeg


## 資料展示

- [download notebook](https://lab.das.twcc.ai/analytics/notebooks/v2/67d82afc-c9f7-4a3d-9d9f-5360c24bea08/view?access_token=6b600e659809a5fedda44dcdb0e34c2a91080d89858b60bb30dc11c697e9d1a1)

* 內容--資料觀察
    1. label distribution

        ![](image/label_distribution.png)

    2. preview images

        ![](image/preview_images.png)



## 訓練模型
- [download notebook](https://lab.das.twcc.ai/analytics/notebooks/v2/e970a7c9-f44b-4cff-aff6-09e43998f1fd/view?access_token=f53e3b189ba471a6a1c9cfee13dc50fe7f01ca9c4afc2e9aa20578bba178b6dd)

* 內容
    1. Dataloader
    2. Training 
    3. Plot results

        * accuracy comparison

            ![](image/accuracy_compare.png)

        * confusion matrix

            ![](image/confusion_matrix.png)


## 模型佈署
- [download notebook](https://lab.das.twcc.ai/analytics/notebooks/v2/4e0ce7dd-a305-4479-ad36-7c1d19a5634d/view?access_token=80e6c779359c4301ae0d5081c2e01bba626f9e46b7a0ff35001e4cef7d04ce75)


* 佈署流程

![](image/deploy_flow.png)

* 內容
    1. load Pytorch model
    2. convert to pytorch_onnx model format
    3. compress model
    4. create model artiface
    5. get deployment space id
    6. create deployment
    7. evaluation

## Reference
* Specifying a model type and software specification
https://www.ibm.com/support/producthub/icpdata/docs/content/SSQNUZ_latest/wsj/wmls/wmls-deploy-python-types.html
