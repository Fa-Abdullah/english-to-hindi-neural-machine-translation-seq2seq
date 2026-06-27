# English to Hindi Neural Machine Translation

A deep learning project that translates English sentences into Hindi using a **Sequence-to-Sequence (Seq2Seq)** architecture with **LSTM** networks implemented in TensorFlow/Keras. The model follows the Encoder–Decoder paradigm for Neural Machine Translation (NMT).

---

## Features

* Sequence-to-Sequence (Seq2Seq) architecture
* Encoder–Decoder LSTM model
* Word Embedding layers
* English to Hindi translation
* Text preprocessing and tokenization
* Trained on parallel bilingual sentence pairs

---

## Dataset

The model is trained using the **Hindi-English Truncated Corpus**, specifically the **TED Talks** subset containing aligned English-Hindi sentence pairs.

### Dataset Information

| Property                | Value     |
| ----------------------- | --------- |
| Source                  | TED Talks |
| Sentence Pairs          | 39,881    |
| Training Split          | 80%       |
| Test Split              | 20%       |
| Maximum Sentence Length | 20 words  |

---

## Model Architecture

```text
English Sentence
        │
Encoder Embedding
        │
Encoder LSTM
        │
Context Vector
        │
Decoder LSTM
        │
Dense + Softmax
        │
Hindi Translation
```

---

## Training Configuration

| Parameter        | Value                    |
| ---------------- | ------------------------ |
| Optimizer        | Adam                     |
| Loss Function    | Categorical Crossentropy |
| Epochs           | 100                      |
| Batch Size       | 128                      |
| Latent Dimension | 300                      |

---

## Text Preprocessing

The preprocessing pipeline includes:

* Lowercasing text
* Removing punctuation and special characters
* Removing digits
* Removing extra spaces
* Adding **START** and **END** tokens to target sentences
* Vocabulary creation
* Integer tokenization
* Sequence padding

---

## Performance

The model successfully learns English-to-Hindi sentence translation through supervised sequence learning.

> **Note:** The training loss is significantly lower than the validation loss, suggesting potential overfitting. Incorporating techniques such as dropout, attention mechanisms, or additional data may improve generalization.

---

## Technologies Used

* Python
* TensorFlow / Keras
* NumPy
* Pandas
* Scikit-learn
* Matplotlib
* Seaborn

---
