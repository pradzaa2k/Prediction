# Stock Price Prediction

We developed the project in two parts:
1. First, we predicted stock price using the LSTM neural network.
2. Then we will build a dashboard using Plotly dash for stock analysis.



Datasets:

To build the stock price prediction model, we used the NSE TATA GLOBAL dataset, ADANIPORTS, BHARATIAIRTEL, INFOSYS, HDFC dataset from Kaggle 


In the Stock Price Analysis dashboard we have predicted the prices of 5 companies (Tata, HDFC Bank, Adani Ports, Bharti Airtel, Infosys). Users have the option to select a specific company tab wherein the actual and predicted price of the company stocks is shown. We also have a separate section to enable users to perform technical chart analysis on various stocks. The user can compare historical performance of a stock against other companies to help him make more calculated decisions.



Design:

● Set Up Infrastructure
1. iPython Notebook
2. Incorporate required Libraries (Keras, Tensor flow, Pandas, Matplotlib,
Sklearn, Numpy, Plotly, Dash)
3. Git project organization

● Prepare Dataset
1. Incorporate data of the required companies
2. Process the requested data into Pandas Dataframe
3. Develop function for normalizing data
4. Dataset used with a 80/20 split on training and test data across all models

● Develop Basic LSTM Model
Set up basic LSTM model with Keras utilizing parameters

● Improve LSTM Model
Develop, document, and compare results using additional labels for the
LSMT model . Document and Visualize Results

● Plot Actual, Benchmark Predicted Values, and LSTM Predicted Values per time series
   
● Analyze and describe results for report.
   
For this project measure of performance will be using the Mean Squared Error (MSE) and Root Mean Squared Error (RMSE) calculated as the difference between predicted and actual values of the target stock at adjusted close price and the delta between the performance of the benchmark model (Linear Regression) and our primary model (Deep Learning).



Algorithm used:

The goal of this project was to study time-series data and explore as many options as possible to accurately predict the Stock Price. Recurrent Neural Nets (RNN) are used specifically for sequence 8 and pattern learning. As they are networks with loops in them, allowing information to persist and thus ability to memorise the data accurately. But Recurrent Neural Nets have a vanishing gradient descent problem which does not allow it to learn from past data as was expected. The remedy of this problem was solved in Long-Short Term Memory Networks, usually referred as LSTMs. These are a special kind of RNN, capable of learning long-term dependencies.In addition to adjusting the architecture of the Neural Network, the following full set of parameters can be tuned to optimize the prediction model:

• Input Parameters

• Preprocessing and Normalization

• Neural Network Architecture

• Number of Layers

• Number of Nodes

• Training Parameters

• Training / Test Split (how much of dataset to train versus test model on; kept constant at 80%
and 20% for benchmarks and lstm model)

• Validation Sets

• Batch Size

• Optimizer Function

• Epochs


Advantages of LSTM:

The main advantage of an LSTM is its ability to learn context - specific temporal dependence. Each LSTM unit remembers information for either a long or a short period of time without explicitly using an activation function within the recurrent components. An important fact to note is that any cell state is multiplied only by the output of the forget gate,which varies between 0 and 1. That is, the forget gate in an LSTM cell is responsible for both the weights and the activation function of the cell state. Therefore, information from a previous cell state can pass through a cell unchanged instead of increasing or decreasing exponentially at each time-step or layer, and the weights can converge to their optimal values in a reasonable amount of time.This allows LSTM to solve the vanishing gradient problem–since the value stored in a memory cell isn't iteratively modified, the gradient does not vanish when trained with backpropagation.
