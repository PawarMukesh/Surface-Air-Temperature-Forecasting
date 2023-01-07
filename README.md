# AI PROJECT ON SURFACE AIR TEMPREATURE  Monthly-Mean

## BUSINESS CASE: BASED ON MEAN TEMPREATURE OF PAST MONTH WE NEED TO PREDICT THE NEXT MONTH SURFACE AIR TEMPRETURE

Surface air temperature is the temperature of the air around us, generally measured at a height of around two meters (about 6 and a half feet) above the surface. Thermometers, shielded from direct solar energy, are used to measure surface air temperature.

![image](https://user-images.githubusercontent.com/101791322/211160165-9cd1957c-9ea8-49b3-b2fb-3b1a1bc32fe3.png)

## PYTHON IMPLIMENTATION:

•	Load Data 
•	Check The Basics of data

### Visualise Trend of Surface Air Temperature:

![image](https://user-images.githubusercontent.com/101791322/211160198-46c0643b-5e46-48e5-9387-78e786994f9c.png)

**Observation:**
- The Data is shows the strong Seasonality.

### Visualise the different components like seasonal nature, trend for that we are use stats model

![image](https://user-images.githubusercontent.com/101791322/211160286-dfb209ee-ba1f-4468-aac0-1114f4b0accb.png)


**Observation:**
- In The Year of 1996 to 1998 surface air temperature has been suddenly increases.
- In 2014 to 2016 also surface temperature is high
- In This we can clearly see the seasonal pattern in data
- In Residule we can not explain the seasonal pattern and trend because of noise data.

## SPLIT DATA INTO TRAIN & TEST

- Taking last 12 month data for testing and remaining data for training

## SCALE DATA
- Scale the data using Min-Max scaler


## MODEL CREATION

- In this project we are use LSTM to predict the mean of surface air temperature
- Creating a batches of 12 months with the help of timeseries generator
- Create sequential model
- Add LSTM layer with 100 neuron and the activation function is relu
- Add Output layer
- Check summary of model
1. Total params: 40,901
2. Trainable params: 40,901
3. Non-trainable params: 0

## COMPILE & TRAIN MODEL

- Use adam optimizer with loss of mean squared error
- Train model on 100 epoch to get a best result

## VISUALISE THE TRAINING LOSS

![image](https://user-images.githubusercontent.com/101791322/211160361-39f30ddc-833f-4ea0-9c79-02d56e633ed3.png)

## MODEL SAVEING
- Save trained model using .h5 extension

## PREDICTION
- Take last 12 months values to make a prediction of first value of test set
- Reshape the data and make prediction

## CHALLENGES:
- Problem Faced To Understand the Business case
- First time worked with time series data
- Problem faced to make prediction 

## LEARNING FROM THIS PROJECT:
- Learn time series prediction using LSTM 
- Learn how to do monthly prediction.




