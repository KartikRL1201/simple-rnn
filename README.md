# IMDB Sentiment Analysis using Simple RNN

A binary sentiment classification model trained on the IMDB movie reviews dataset using a Simple Recurrent Neural Network (RNN), accompanied by a Streamlit web application for real-time predictions.

## Project Structure

```
├── embedding.ipynb       # Word embedding demonstrations and experiments
├── simplernn.ipynb       # Model training, validation, and evaluation
├── prediction.ipynb      # Standalone inference and test script
├── simplernn_model.keras # Saved trained Keras model
├── main.py               # Streamlit web application
└── requirements.txt      # Project dependencies
```

## Model Architecture

- **Embedding Layer:** Input vocabulary of 10,000 words mapped to 128-dimensional dense vectors (input sequence length: 500).
- **SimpleRNN Layer:** 128 hidden units with `tanh` activation.
- **Output Layer:** Single dense unit with `sigmoid` activation for binary classification (Positive / Negative).
- **Loss & Optimizer:** Binary Cross-Entropy optimized via Adam.

## Setup & Installation

1. Clone the repository and navigate to the project directory:
   ```bash
   git clone <repo-url>
   cd simple-rnn
   ```

2. Create and activate a virtual environment (optional but recommended):
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. Install required packages:
   ```bash
   pip install -r requirements.txt
   ```

## Usage

### 1. Training the Model
Open and execute `simplernn.ipynb` to download the IMDB dataset, preprocess the text, train the RNN, and export the trained model (`simplernn_model.keras`).

### 2. Running the Web App
Launch the Streamlit app locally:
```bash
streamlit run main.py
```
Open the provided local URL in your browser, enter any review text, and click **Predict** to view the sentiment classification and prediction confidence.

