# Company name duplicates

**NLP study case**: check if company name is duplicate of another one or not just by name.

## Datasets

- The dataset `data/train.scv` is provided by mentors within the course.

## Project info and structure

The Jupyter notebooks contain training of two models: a long short-term memory RNN (LSTM) and pretrained transformer BERT — as well as EDA (most in bert.ipynb). You can reproduce the experiment by following the installing dependencies instructions below.

Detailed working directory structure presentation.

```text
.
├── data                    <- The files including data and images 
│   ├── README_files        <- The images for README design
│   └── train.csv           <- The project data
├── notebooks               <- The Jupyter notebooks' folder containing training and analysis
│   ├── BERT
│   │   └── bert.ipynb      <- The Jupyter notebook containing the BERT model training  
│   ├── LSTM              
│   │   ├── board_loss      <- The Train/Test loss evolution traking during the training
│   │   └── lstm.ipynb      <- The Jupyter notebook containing the LSTM model training  
├── weights                 <- The weights of trained models
├── .gitignore              <- The Gitignore configuration
├── LICENSE                 <- The MIT License file
├── README.md               <- The top-level README file
├── get_weights.sh          <- The script for downloading weights
└── requirements.txt        <- The requirements file for reproducing the experiment

```

## Metrics

Metrics represented by ROC curves and Precision-recall curves speak for themselves.

### LSTM

![LSTM results demonstration](/data/README_files/LSTM_results.PNG "LSTM results demonstration")

`AUC = 0.983`

### BERT

![BERT results demonstration](/data/README_files/BERT_results.PNG "BERT results demonstration")

`AUC = 0.997`

## Installation and dependencies

### Dependencies

Dependencies are managed with `requirements.txt`.

```python
pip install -r requirements.txt 
```

### Models weights setting

#### For Linux users

1. After cloning the repo, open the terminal in the root directory

2. Give the execution rights to the script:

    ```bash
    sudo chmod +x get_weights.sh
    ```

3. Run the script:

    ```bash
    sh get_weights.sh
    ```

After the procedure your weights' directory structure must look like this:

```text
.
├── weights
│   ├── BERT
│   │   └── saved_model
│   ├── LSTM
│   │   ├── lstm_4_epochs
│   │   └── lstm_15_epochs

```

If something goes wrong you could use an alternative way. Check the next section for details.

#### For Windows users

Follow the link to gdrive [weights](https://drive.google.com/drive/folders/1oG8aWS5Z2Dplg6Ixjb5tcfBUJStMaKUy?usp=sharing), download and unpack the content so the weights' directory looks exactly as it shown above.
