# Machine-Learning-with-Python-Projects---Neural-Network-SMS-Text-Classifier

# SMS Spam Classifier

This project is a machine learning model designed to classify SMS messages as either **"ham"** (normal messages) or **"spam"** (unwanted or promotional messages). It uses the SMS Spam Collection dataset and applies natural language processing techniques to achieve accurate classification.

## Features
- **Input**: A text message string.
- **Output**: A prediction indicating whether the message is "ham" or "spam", along with the probability.

Example output:
```
Input: "how are you doing today?"
Output: [0.01, "ham"]
```

## Project Structure
1. **Data Loading**: The project uses pre-labeled training and testing datasets provided in TSV format.
2. **Preprocessing**: Tokenization and padding of text messages for use in the model.
3. **Model Architecture**: A neural network with:
   - Embedding layer
   - LSTM layers
   - Dense layers for binary classification
4. **Function**: A `predict_message` function to classify any given SMS message.
5. **Testing**: Includes a pre-defined test suite to validate the model's performance.

## Installation
To run this project locally, follow these steps:

1. Clone the repository:
   ```bash
   git clone <repository-url>
   cd <repository-folder>
   ```

2. Install the required Python packages:
   ```bash
   pip install tensorflow pandas numpy matplotlib
   ```

3. Download the dataset files:
   ```bash
   wget https://cdn.freecodecamp.org/project-data/sms/train-data.tsv
   wget https://cdn.freecodecamp.org/project-data/sms/valid-data.tsv
   ```

## How to Use
1. Open the notebook or Python script containing the code.
2. Run all cells to train the model.
3. Use the `predict_message` function to classify messages:
   ```python
   pred_text = "You have won $1000! Call now to claim your prize."
   prediction = predict_message(pred_text)
   print(prediction)  # Output: [0.95, 'spam']
   ```

## Dataset
The dataset is sourced from the [SMS Spam Collection](https://www.kaggle.com/uciml/sms-spam-collection-dataset). It consists of labeled messages:
- **ham**: Regular messages
- **spam**: Unwanted or promotional messages

## Model
- **Embedding Layer**: Converts text to dense vector representations.
- **LSTM Layers**: Capture sequential dependencies in text.
- **Dense Layers**: Perform binary classification.
- **Output**: A probability value and corresponding label ("ham" or "spam").

## Testing
A pre-defined test suite validates the model's performance. If all test cases pass, the following message is displayed:
```
You passed the challenge. Great job!
```

## License
This project is open-source and available under the [MIT License](LICENSE).

---

Feel free to contribute to the project or raise issues if you find any bugs or have suggestions for improvement!
