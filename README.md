# SemEval2020

## Sub-task A

Offensive Speech Detection

### Set/Model 4 Folds F1-Scores

| Set       | TF-IDF with SVM | ML-DistilBert | Bi-GRU with Attention | Word-CNN model        | BERT-CNN model        |
|:---------:|:---------------:|:-------------:|:---------------------:|:---------------------:|:---------------------:|
| Arabic    | 0.63            | 0.64          | 0.68                  | __0.71__  (word2vec)  | -                     |
| Danish    | 0.46            | 0.42          | 0.47                  | __0.54__              | 0.45 (No fine-tuning) |
| Greek     | 0.60            | 0.69          | 0.60                  | 0.61                  | __0.75__              |
| Turkish   | 0.40            | 0.54          | 0.52                  | 0.49                  | __0.70__              |

### Baseline Scores: (TF-IDF with SVM)

| Set       | Precision | Recall   | F1-Score |
|:---------:|:---------:|:--------:|:--------:|
| Arabic    | 0.66      | 0.60     | 0.63     |
| Danish    | 0.48      | 0.43     | 0.46     |
| Greek     | 0.67      | 0.55     | 0.60     |
| Turkish   | 0.72      | 0.28     | 0.40     |

### ML-DistilBert Scores:

| Set       | Precision | Recall   | F1-Score |
|:---------:|:---------:|:--------:|:--------:|
| Arabic    | 0.68      | 0.60     | 0.64     |
| Danish    | 0.78      | 0.29     | 0.42     |
| Greek     | 0.77      | 0.62     | 0.69     |
| Turkish   | 0.69      | 0.44     | 0.54     |

### Bi-GRU with Attention Scores:

| Set       | Precision | Recall   | F1-Score |
|:---------:|:---------:|:--------:|:--------:|
| Arabic    | 0.74      | 0.63     | 0.68     |
| Danish    | 0.59      | 0.39     | 0.47     |
| Greek     | 0.66      | 0.55     | 0.60     |
| Turkish   | 0.62      | 0.44     | 0.52     |

### Word-CNN Scores:

| Set       | Precision | Recall   | F1-Score |
|:---------:|:---------:|:--------:|:--------:|
| Arabic    | 0.86      | 0.63     | 0.73     | 
| Danish    | 0.81      | 0.41     | 0.54     |
| Greek     | 0.71      | 0.55     | 0.62     |
| Turkish   | 0.62      | 0.40     | 0.49     |

<!--
Arabic concatenate with aravec
max_features = 30000
max_char_features = 512
learning_rate = 5e-4
embed_size = 256
char_embed_size = 512
batch_size = 32
maxlen = 32
maxcharlen = 128
epochs = 4
folds = 4
seed = 1234
-->

### Final Model

| Set                           | Precision | Recall   | F1-Score |
|:-----------------------------:|:---------:|:--------:|:--------:|
| Greek   (Bert)                | 0.81      | 0.65     | 0.73     |
| Greek   (Bert-CNN)            | 0.80      | 0.71     | 0.75     |
| Greek   (Bert-tuned-CNN)      | 0.76      | 0.76     | 0.76     |
| Danish  (Bert)                | 0.67      | 0.28     | 0.39     |
| Danish  (Bert-CNN)            | 0.67      | 0.33     | 0.44     |
| Danish  (CNN)                 | 0.81      | 0.41     | 0.54     |
| Turkish (Bert)                | 0.76      | 0.63     | 0.69     |
| Turkish (Bert-CNN)            | 0.70      | 0.70     | 0.70     |
| Arabic  (Bert-CNN)            | 0.81      | 0.75     | 0.78     |
| Arabic  (CNN "Aravec+Bert")   | 0.85      | 0.76     | 0.80     |