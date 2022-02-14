# Aeolian-Drone-Project

Drone is promissing for last-mile delivery application but inefficient in terms of energy consumption. This project aims at predicting and optimising drone's battery usage. The data used comes from a publicly published flight test study of drones.

<img src="/images/Image1.png">
<img src="/images/Image4.png" width=300 height=300>

I have prepared and studied the data and used machine learning (XGBoost), unsupervised learning (k-Nearest Neighbors) and deep learning (LSTM) for modeling. The unsupervised learning model identifies various flight phases in the training data which is then used as a feature. Another feature which is extracted is the local wind (using measured data or weather API).

<img src="/images/Image6.png">

These features together with the operational data e.g. payload weight, programmed height and cruise speed are then used to train the machine learning model that can predict the average power consumption in each phase of flight (and total battery usage depending on the flight schadual).

<img src="/images/modeling_results.png">

I have also developed an app using the machine learning predictor model, named as Aeolus, which receives the operational data, queries for the local wind speed at the flight level and predicts the battery usage.

<img src="/images/Aeolus.png" width=300 height=300>

https://github.com/AmirShakouri19/Aeolian-Drone-Project/blob/main/images/Aeolus.mp4


Finally, I am developing a deep learning model (LSTM) which is going to basically identify the temporal (instantanous) drone power consumption - not time-averaged. This model aims to further investigate the stochastic nature of the problem with resepect to wind and the shifts between various phases of the flight. 
For further explanation please refer to the Main.ipynb. The contents of this project is getting updated...    



