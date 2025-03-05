# codealpha_tasks

TASK-1  STOCK PRICE PREDICTION
      Building the LSTM Model
Adding Layers:

First LSTM layer: Captures sequential patterns with 50 neurons and return_sequences=True to pass output to the next LSTM layer.

Second LSTM layer: Another 50 neurons, but with return_sequences=False as it's the last LSTM layer.

Two dense (fully connected) layers: One with 25 neurons and another with 1 neuron for the final predicted value.

Compiling the Model:

Adam optimizer: Used for updating weights efficiently.

mean_squared_error loss: Measures how well the model's predictions match the actual data.

Training:

The model is trained with a batch size of 1 and for only 1 epoch (one complete pass through the data).

Testing the Model
Test Data Preparation:

A new dataset, test_data, includes the last 60 data points from train_data and all of test_data.

The data is split into x_test (input sequences) and y_test (actual prices for comparison).

Reshaping Test Data:

x_test is reshaped similarly to x_train to match the LSTM input structure.

Making Predictions:

The model predicts stock prices using x_test.

The predicted values are scaled back to the original range using scaler.inverse_transform.

Visualization
Training and Validation Split:

The original dataset is split into train (training data) and valid (validation/testing data).

valid includes the true prices as well as the model's predicted values (Predictions).

Plotting:

The plot displays:

Training prices: Historical stock prices used for training.

Validation prices: Actual prices for the testing period.

Predicted prices: Model's predictions for the testing period.

Helps visually evaluate the model's accuracy.
