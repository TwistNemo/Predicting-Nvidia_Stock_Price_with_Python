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
    <li><strong>Enhanced Feature Engineering:</strong> Incorporate additional features such as trading volume, technical indicators, and sentiment analysis from news and social media.</li>
    <li><strong>Data Augmentation:</strong> Improve data quality and quantity by including more historical data and ensuring the dataset is clean and comprehensive.</li>
</ul>

<h2 id="how-to-run-the-code">How to Run the Code</h2>
<p>To run the code, follow these steps:</p>
<ol>
    <li><strong>Clone the Repository:</strong>
        <pre><code>git clone https://github.com/yourusername/nvidia-stock-price-prediction.git
cd nvidia-stock-price-prediction
</code></pre>
    </li>
    <li><strong>Open the Notebook in Google Colab:</strong>
        <ul>
            <li>Go to <a href="https://colab.research.google.com/">Google Colab</a>.</li>
            <li>Upload the Jupyter notebook (<code>Predicting_NVIDIA_Stock_Price_with_Python_By_Tanjela.ipynb</code>) from this repository.</li>
        </ul>
    </li>
    <li><strong>Install Required Libraries:</strong>
        <p>In the first cell of the notebook, ensure you have the required libraries installed. If not, install them using:</p>
        <pre><code>!pip install pandas numpy matplotlib seaborn scikit-learn tensorflow</code></pre>
    </li>
    <li><strong>Run the Notebook:</strong>
        <p>Execute each cell in the notebook sequentially and follow the instructions within the notebook for any specific configurations or data preprocessing steps.</p>
    </li>
</ol>
<p>By following these steps, anyone can replicate the process and run the code to predict NVIDIA's stock price.</p>

<hr>
<h3>Screenshot of code running in the git repo
    ![image](https://github.com/user-attachments/assets/d7f6ae47-c1d3-4503-ad49-0b2a814f798f)

</h3>


