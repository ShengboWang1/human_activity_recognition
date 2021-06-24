

# How to run the code

## Human activity recognition
Train model:

`python3 main.py --train=True  --model_name='multi-rnn' --device_name='iss GPU' --kernel_initializer='he_normal'`

Evaluate model:

`python3 main.py --train=False  --model_name='multi-rnn' --device_name='iss GPU' --kernel_initializer='he_normal'`

Ensemble learning, evaluate and visualization:

`python3 ensemble.py`

# Results
Please see details in  presentation slides.


## Human activity recognition
Results of ensemble model with He_normal Glorot_uniform and Glorot_normal initializers:
| Architecture | LSTM | GRU |
| :---: | :---: | :---: |
| Test Accuracy | 91.73% | 94.48% | 

Corresponding Hyperparameters for the best GRU-based model:

| GRU layers | Dense layers | GRU units | Dense units | Window size | Shift size | Dropout rate | Val accuracy |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
| 2 | 3 | 512 | 256 | 250 | 125 | 0.471 | 92.9% |


Visualization of test label and predictions:

![01_acc_true](https://github.tik.uni-stuttgart.de/iss/dl-lab-2020-team06/blob/master/results/02_har/01_acc%20signals%20with%20true%20labels%20visualization.png)
![02_acc_pred](https://github.tik.uni-stuttgart.de/iss/dl-lab-2020-team06/blob/master/results/02_har/02_acc%20signals%20with%20predictions%20visualization.png)
![03_gyro_true](https://github.tik.uni-stuttgart.de/iss/dl-lab-2020-team06/blob/master/results/02_har/03_gyro%20signals%20with%20true%20labels%20visualization.png)
![04_gyro_pred](https://github.tik.uni-stuttgart.de/iss/dl-lab-2020-team06/blob/master/results/02_har/04_gyro%20signals%20with%20predictions%20visualization.png)
![05_colormap](https://github.tik.uni-stuttgart.de/iss/dl-lab-2020-team06/blob/master/results/02_har/05_colormap.png)


Confusion Matrix:
![cm_6](https://github.tik.uni-stuttgart.de/iss/dl-lab-2020-team06/blob/master/results/02_har/cm_6.png)


Normalised confusion matrix:
![normal_cm_6](https://github.tik.uni-stuttgart.de/iss/dl-lab-2020-team06/blob/master/results/02_har/normal_cm_6.png)


