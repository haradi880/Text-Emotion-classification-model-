HaradiBots Text Emotion Classification Model

A transformer-based emotion classification model trained on the GoEmotions dataset using DistilBERT.

The model detects human emotions from text using Natural Language Processing (NLP) and deep learning.


---

Model Links

Fine-Tuning Notebook

[Fine-Tuning Code](https://www.kaggle.com/code/haradibots/import-path?utm_source=chatgpt.com)

Trained Model

[Text Emotion Classification Model](https://www.kaggle.com/models/haradibots/text-emotion-classification-model/PyTorch/default/1?utm_source=chatgpt.com)

Testing Notebook

[Testing Notebook](https://www.kaggle.com/code/haradibots/test-the-text-emotion-classification-model/notebook?utm_source=chatgpt.com)


---

Preview


---

Features

Transformer-based NLP model

Fine-tuned DistilBERT architecture

28 emotion categories

Real-time emotion prediction

Kaggle GPU training support

Hugging Face Transformers integration

PyTorch backend

Deployable for chatbot and robotics systems



---

Emotion Labels

admiration
amusement
anger
annoyance
approval
caring
confusion
curiosity
desire
disappointment
disapproval
disgust
embarrassment
excitement
fear
gratitude
grief
joy
love
nervousness
optimism
pride
realization
relief
remorse
sadness
surprise
neutral


---

Model Information

Property	Value

Model Name	HaradiBots Emotion Classifier
Base Model	distilbert-base-uncased
Framework	PyTorch
NLP Library	Transformers
Dataset	GoEmotions
Training Platform	Kaggle
GPU Support	Tesla T4 / P100
Task	Text Emotion Classification



---

Dataset

Dataset used:

GoEmotions

Created by: Google

Official Dataset: [GoEmotions Dataset](https://github.com/google-research/google-research/tree/master/goemotions?utm_source=chatgpt.com)

The dataset contains Reddit comments labeled with multiple human emotions for emotion understanding research. 


---

Installation

pip install transformers datasets torch scikit-learn kagglehub


---

Load The Model

from transformers import (
    AutoTokenizer,
    AutoModelForSequenceClassification,
    pipeline
)

MODEL_PATH = "/kaggle/input/models/haradibots/text-emotion-classification-model/pytorch/default/1/emotion_model"

tokenizer = AutoTokenizer.from_pretrained(MODEL_PATH)

model = AutoModelForSequenceClassification.from_pretrained(MODEL_PATH)

classifier = pipeline(
    "text-classification",
    model=model,
    tokenizer=tokenizer,
    top_k=None
)


---

Example Usage

text = "I feel very happy today!"

result = classifier(text)

print(result)


---

Example Output

joy : 0.8145
excitement : 0.0549
gratitude : 0.0219


---

Model Architecture

Input Text
    ↓
Tokenizer
    ↓
DistilBERT Encoder
    ↓
Classification Head
    ↓
Emotion Prediction


---

Example Emotional Tests

Input:
"Sorry I think I messaged too much"

Prediction:
remorse

Input:
"I finally achieved the thing I worked on for years, but somehow I still feel empty inside."

Prediction:
sadness / disappointment

Input:
"Kush ho akele toh kush raho sorry for disturbance 🥀🙂🙏🏽"

Prediction:
remorse / sadness


---

Future Improvements

Planned upgrades:

Multi-label emotion detection

Emotion-aware chatbot integration

Voice emotion recognition

Sarcasm detection

Emotional memory systems

Real-time conversation tracking

Flask/FastAPI deployment

Robotics and humanoid AI integration



---

Technologies Used

[PyTorch](https://pytorch.org/?utm_source=chatgpt.com)

[Transformers by Hugging Face](https://huggingface.co/docs/transformers/index?utm_source=chatgpt.com)

[KaggleHub](https://pypi.org/project/kagglehub/?utm_source=chatgpt.com)

Kaggle GPU Infrastructure



---

Author

Aditya

Project developed for NLP research, emotional AI systems, conversational intelligence, and humanoid robotics.


---

License

This project is open for educational and research purposes.