<h1 align="center">BATPredict</h1>

<p align="center">
  <b><i>Recurrent Neural Network</i></b> and <b><i>Long Short-Term Memory.</i></b><br><br>
  <img src="https://img.shields.io/badge/Flask-000000?style=for-the-badge&logo=flask&logoColor=white"> <img src="https://img.shields.io/badge/Jinja-000000?style=for-the-badge&logo=jinja&logoColor=white"> <img src="https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white"> <img src="https://img.shields.io/badge/JavaScript-323330?style=for-the-badge&logo=javascript&logoColor=F7DF1E"> <img src="https://img.shields.io/badge/jQuery-0769AD?style=for-the-badge&logo=jquery&logoColor=white"><br>
<img src="https://img.shields.io/badge/Python-FFD43B?style=for-the-badge&logo=python&logoColor=blue"> <img src="https://img.shields.io/badge/Keras-C50000?style=for-the-badge&logo=keras&logoColor=white">
</p>

## Overview 

Will predict the close value of the Basic Attention Token currency based on its open value.

![CryptoCurrency png](https://github.com/Scylidose/BATPredict/blob/master/img/crypto_bat-img.png)  

## Features

- Display close value for the current day based of the open value.  

- Show diverse plot values from the last 30 days.  

- Show algorithm accuracy based on last year close value.  


## How to use

To clone and run this application, you'll need Git and Flask installed on your computer. From your command line:

```bash
# Retrieve git folder
$ git clone https://github.com/Scylidose/BATPredict.git

$ cd BATPredict/

# Install dependencies 
$ pip3 install -r requirements.txt

# Run application
$ make run
```

You can then access the application with the given address.  

## Data Steps

### Fetch Data

- Get Comma-separated values (csv) file everyday containing values about the Basic Attention Token cryptocurrency from the **yfinance** module (Yahoo Finance, https://finance.yahoo.com/quote/BAT-CAD/history). The data is ranged between the day BAT was published until the day the file is downloaded.  

### Pre-process Data

- Removed non-informative columns and Not Available data rows.  

- Scaled Open and Close values with a MinMax Scaler.  


### Data Exploration

- Plot of open and close values per day (for the last 30 days).  

- Plot of highest and lowest values per day (for the last 30 days).  

- Plot of the volume values per day (for the last 30 days).  

- Plot of the close value from last year until today.   

### Model

- Recurrent Neural Network :  
    - LSTM -> 150 Units  
    - Dropout -> Probability of 0.3  
    - LSTM -> 150 Units  
    - Dropout -> Probability of 0.3  
    - LSTM -> 150 Units  
    - Dropout -> Probability of 0.3  
    - Dense -> 1 Unit  
- Optimizer -> Adam  
- Loss -> Mean Squarred Error

### Accuracy

- R2 Score.  


