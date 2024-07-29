<h1>Predicting NVIDIA Stock Price with Python</h1>

<p>This repository contains the code for predicting NVIDIA's stock price using a Long Short-Term Memory (LSTM) neural network. The project is implemented in a Jupyter notebook and executed on Google Colab.</p>

<h2>Table of Contents</h2>
<ul>
    <li><a href="#introduction">Introduction</a></li>
    <li><a href="#data-acquisition-and-preprocessing">Data Acquisition and Preprocessing</a></li>
    <li><a href="#model-selection-and-training">Model Selection and Training</a></li>
    <li><a href="#evaluation-and-prediction">Evaluation and Prediction</a></li>
    <li><a href="#visualization">Visualization</a></li>
    <li><a href="#limitations-of-the-model">Limitations of the Model</a></li>
    <li><a href="#potential-improvements">Potential Improvements</a></li>
    <li><a href="#how-to-run-the-code">How to Run the Code</a></li>
</ul>

<h2 id="introduction">Introduction</h2>
<p>This project aims to predict the future stock prices of NVIDIA using historical stock price data. The model used for this purpose is a Long Short-Term Memory (LSTM) neural network, which is well-suited for time series forecasting.</p>

<h2 id="data-acquisition-and-preprocessing">Data Acquisition and Preprocessing</h2>
<p>The NVIDIA stock price data is loaded into a pandas DataFrame. The initial steps include displaying the first and last few rows of the DataFrame to understand its structure. Exploratory Data Analysis (EDA) is performed to visualize the closing prices over time. Statistical features such as rolling means and standard deviations are computed, and missing values are handled to ensure the dataset's completeness. Feature engineering steps introduce lag features and rolling statistics to enrich the data for model training.</p>

<h2 id="model-selection-and-training">Model Selection and Training</h2>
<p>A Long Short-Term Memory (LSTM) neural network is chosen for its effectiveness in time series prediction tasks. The LSTM model is constructed using the <code>Sequential</code> API from <code>Keras</code>, with layers added to capture sequential dependencies in the stock price data. The model is compiled with the Adam optimizer and mean squared error loss function. The training process includes early stopping to prevent overfitting, monitoring validation loss to determine the optimal number of training epochs.</p>

<h2 id="evaluation-and-prediction">Evaluation and Prediction</h2>
<p>The model's performance is evaluated on both the training and testing datasets. Predictions are made using the trained LSTM model, and the predicted values are transformed back to the original scale for comparison. The evaluation metrics include Mean Absolute Error (MAE) and Mean Squared Error (MSE) for both training and testing datasets.</p>

<h2 id="visualization">Visualization</h2>
<p>Actual vs. predicted stock prices are plotted to visually assess the model's performance. Separate plots are created for training and testing periods, with clear markers indicating actual values and predictions. The visualization includes annotations for the train/test split and other relevant details to enhance interpretability.</p>

<h2 id="limitations-of-the-model">Limitations of the Model</h2>
<ul>
    <li><strong>Limited Feature Engineering:</strong> The model primarily uses basic lag features and rolling statistics, missing out on other influential factors like market sentiment and economic indicators.</li>
    <li><strong>Data Quality and Quantity:</strong> The dataset may have limitations in terms of length, granularity, and completeness, impacting the model's performance.</li>
</ul>

<h2 id="potential-improvements">Potential Improvements</h2>
<ul>
    <li><strong>Regularization and Hyperparameter Tuning:</strong> Implement regularization techniques (e.g., dropout) and perform extensive hyperparameter tuning to reduce overfitting.</li>
    <li><strong>Enhanced Feature Engineering:</strong> Incorporate additional features such as trading volume, technical indicators
