# QUnet

#### Lung Segmentation
1- Download the Lung Segmentation dataset from [Kaggle](https://www.kaggle.com/kmader/finding-lungs-in-ct-data/data) link and extract it. </br>
2- Run `Prepare_data.py` for data preperation, train/test seperation and generating new masks around the lung tissues.
3- Run `train_lung.py` for training BCDU-Net model using trainng and validation sets (20 percent of the training set). The model will be train for 50 epochs and it will save the best weights for the valiation set. You can train either BCDU-net model with 1 or 3 densly connected convolutions. </br>
4- For performance calculation and producing segmentation result, run `evaluate_performance.py`. It will represent performance measures and will saves related figures and results.</br>

## Lung Segmentation

#### Performance Evalution on the Lung Segmentation task

Methods | Year |F1-scores | Sensivity| Specificaty| Accuracy | AUC | JS 
------------ | -------------|----|-----------------|----|---- |---- |---- 
Ronneberger and etc. all [U-net](https://arxiv.org/abs/1505.04597)	     	    |2015   | 0.9658	|0.9696	  |0.9872	  |0.9872  |0.9784 |0.9858
Alom  et. all [Recurrent Residual U-net](https://arxiv.org/abs/1802.06955)	|2018	  | 0.9638 |0.9734 |0.9866 |0.9836	  |0.9800	  |0.9836
Alom  et. all [R2U-Net](https://arxiv.org/ftp/arxiv/papers/1802/1802.06955.pdf)	        |2018	  | 0.9832	|**0.9944**	  |0.9832	  |0.9918	  |0.9889 | 0.9918
Azad et. all [Proposed BCDU-Net](https://github.com/rezazad68/LSTM-U-net/edit/master/README.md)	  |2019 	| 0.9904	|0.9910	  |0.9982	  |0.9972	  |**0.9946**| 0.9972
QUNet  |- | **0.9908** | 0.9912 | **0.9985** | **0.9974** | 0.9915 | **0.9974**





#### Lung Segmentation results
![Lung Segmentation result](https://github.com/YimingCuiCuiCui/QUnet/tree/main/Lung_Segmentation/sample_results.png)


