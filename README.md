# Aeolian-Drone-Project

Drone is promissing for last-mile delivery application but inefficient in terms of energy consumption. This project aims at predicting and optimising drone's battery usage. The data used comes from a publicly published flight test study of drones:

<img src="/images/Image1.png"><img src="/images/Image4.png" width=200 height=200>


I have prepared and studied the data and used machine learning (XGBoost), unsupervised learning (k-Nearest Neighbors) and deep learning (LSTM) for modeling. The unsupervised learning model identifies various flight phases in the training data which is then used as a feature. Another useful feature which I extracted  - using measured data and/or weather API - is the tailwind (wind in flight direction):

<img src="/images/Image6.png"><img src="/images/Image7.png">

These features together with the operational data e.g. payload weight, programmed height and cruise speed are then used to train the machine learning model that can predict the average power consumption in each phase of flight (and total battery usage depending on the flight schadual).

<img src="/images/modeling_results.png">

I have also developed an app using the machine learning predictor model, named as Aeolus, which receives the operational data, queries for the local wind speed at the flight level and predicts the battery usage.

<img src="/images/Aeolus.png" width=200 height=200>


You can download a demonstration of the app, here:

https://github.com/AmirShakouri19/Aeolian-Drone-Project/blob/main/images/Aeolus.mp4


Finally, I am developing a deep learning model (LSTM) which is going to basically identify the temporal (instantanous) drone power consumption - not time-averaged. This model aims to further investigate the stochastic nature of the problem with resepect to wind and the shifts between various phases of the flight. 
For further explanation please refer to the Main.ipynb. The contents of this project is getting updated...    

You can find the dataset address and the modeling steps I took in the "Main" notebook. Also, the "app" folder include the code for the Aeolus app.

Interested or have questions? Please don't hesitate to comment here or contact me. Also, feel free to fork and contribute to the project...
