# LSTM_stock_predictor

In this assignment, we used deep learning recurrent neural networks to model bitcoin closing prices. One model will use the FNG indicators to predict the closing price while the second model will use a window of closing prices to predict the nth closing price.

### Training and Testing:
* In Fear and Greed model, we used FNG values to predict the closing price. On the other hand, in closing pricce model, we used previous closing price to predict the future price
* In each model, we have considered 70% data for training and 30% data for testing.
* We applied `MinMaxScaler` to the X and y values to scale the data for the model. Lastly, we reshaped the X_train and X_test values to fit the model's requirement of samples, time steps, and features

### Build and train custom LSTM RNNs:
We created and maintained same custom LSTM RNN architecture for both model. In [FNG](https://github.com/Ashfaque-Rahman/LSTM_stock_predictor/blob/main/Starter_Code/lstm_stock_predictor_fng.ipynb) model, we used FNG values to fit the data and in [closing price model](https://github.com/Ashfaque-Rahman/LSTM_stock_predictor/blob/main/Starter_Code/lstm_stock_predictor_closing.ipynb), we fit the data using only closing price

### Evauation:
After successfully runnung both models with lots of different combination of `window_size`, `epochs` and `batch_size`, we found below observations:
    1. [closing price model](https://github.com/Ashfaque-Rahman/LSTM_stock_predictor/blob/main/Starter_Code/lstm_stock_predictor_closing.ipynb) has significantly lower loss than the [FNG](https://github.com/Ashfaque-Rahman/LSTM_stock_predictor/blob/main/Starter_Code/lstm_stock_predictor_fng.ipynb) model
    2. Over time, the closing price model tracks the actual values better
    3. We tried several `window_size`, `epochs` and `batch_size` to find the most efficient model. For our case this was `window_size`=2 and `batch_size`=2

### Closing_Price_Model:
![alt=""](https://github.com/Ashfaque-Rahman/LSTM_stock_predictor/blob/main/Results/closing_price_model.JPG)

### Fear and Greedd Model:
![alt=""](https://github.com/Ashfaque-Rahman/LSTM_stock_predictor/blob/main/Results/fng_model.JPG)

