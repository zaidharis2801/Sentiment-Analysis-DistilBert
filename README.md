
# Custom Sentiment Analysis with DistilBert

This repository contains code for a custom sentiment analysis model. The model uses the DistilBERT transformer from Hugging Face's transformers library for its backend. The data it uses is the SMSSpamCollection dataset, and it is trained to differentiate between 'ham' and 'spam' SMS messages.

## Setup

1. Clone this repository to your local machine.
2. Install the necessary Python packages. This project requires `pandas`, `sklearn`, `tensorflow`, and `transformers`. You can install these with pip:

```sh
pip install pandas sklearn tensorflow transformers
```

## Data

The data for this project is the SMSSpamCollection dataset. It's a collection of SMS messages, labeled 'ham' for normal messages and 'spam' for spam messages. The dataset is read in with pandas, and the message content and labels are extracted into lists.

## Training and Evaluation

The model is trained on the dataset, with 80% of the data used for training and 20% for evaluation. It uses a DistilBERT transformer, with the tokenizer and model both being the 'distilbert-base-uncased' version. The tokenizer is used to encode the messages into a format that the model can use.

The model is trained for two epochs, with various training arguments set for best performance.

After training, the model is evaluated on the test dataset. The evaluation includes a confusion matrix to get a visual idea of the model's performance.

## Usage

To use the trained model, run the included Jupyter notebook. The last cell saves the model to the file 'senti_model', so you can load it in the future without needing to retrain it.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
```
