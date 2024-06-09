# Stock Market Price Prediction

This project is an end-to-end machine learning application developed in Python to predict stock market prices. The project covers data preprocessing, model creation using TensorFlow and Keras, training, testing, and deployment as a real-time web application.

![image](https://github.com/Hairul343/Stock_Prediction_model/assets/140678940/ff27ce36-abb9-4819-aae8-93b50a3f4e57)

![image](https://github.com/Hairul343/Stock_Prediction_model/assets/140678940/08f1b47f-e4e4-4002-8c15-b6171f94914d)


## Project Structure

- `data/`: Contains the dataset files.
- `notebooks/`: Jupyter notebooks for data preprocessing and model training.
- `app/`: Web application code for deployment.
- `requirements.txt`: Lists the dependencies for the project.
- `.gitignore`: Specifies files and directories to be ignored in the repository.

## Project Workflow

1. **Data Collection and Preprocessing**:
    - The historical stock market data is collected and stored in the `data/` directory.
    - Data preprocessing involves cleaning the data, handling missing values, feature scaling, and creating training and testing datasets. This is implemented in Jupyter notebooks located in the `notebooks/` directory.

2. **Model Creation**:
    - The machine learning model is created using TensorFlow and Keras.
    - The model consists of layers such as Dense, Dropout, and LSTM to capture the sequential nature of stock prices.
    - The model architecture is defined in the notebooks under the `notebooks/` directory.

3. **Model Training**:
    - The preprocessed data is used to train the model.
    - Training involves feeding the data into the model and optimizing it to minimize the prediction error.
    - Training scripts and detailed steps are provided in the Jupyter notebooks.

4. **Model Testing**:
    - After training, the model's performance is evaluated using test data.
    - The testing phase ensures that the model generalizes well to unseen data.
    - Testing scripts and evaluation metrics are included in the notebooks.

5. **Model Deployment**:
    - The trained model is saved and deployed as a web application using Flask.
    - The web application allows users to input stock data and get real-time predictions.
    - Deployment code and instructions are in the `app/` directory.

## Installation

To set up the project, follow these steps:

1. Clone the repository:
    ```sh
    git clone https://github.com/Hairul343/Stock_Prediction_model.git
    cd Stock_Prediction_model
    ```

2. Create a virtual environment:
    ```sh
    python -m venv venv
    source venv/bin/activate   # On Windows use `venv\Scripts\activate`
    ```

3. Install the dependencies:
    ```sh
    pip install -r requirements.txt
    ```

## Data Collection

We use the `yfinance` library to fetch historical stock market data. Below is an example of how to use the `yfinance` library to download stock data:

```python
import yfinance as yf

# Define the stock ticker and the time period
ticker = 'AAPL'
start_date = '2010-01-01'
end_date = '2023-01-01'

# Download the stock data
data = yf.download(ticker, start=start_date, end=end_date)

# Save the data to a CSV file
data.to_csv('data/stock_data.csv')
