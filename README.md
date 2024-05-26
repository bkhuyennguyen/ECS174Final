# ECS174Final

### Created by Aroop Biswal, guys put ur names hereee

# Handwriting Similarity Detection

This project is designed to verify if two pieces of handwriting are from the same author using a Siamese network.

## Setup Instructions

### Step 1: Install Prerequisites

#### Option 1: Using Pip
```
pip install -r requirements.txt
```

#### Option 2: Using Conda
```
conda env create -f environment.yml --name handwriting-similarity
conda activate handwriting-similarity
```


### Step 2: Download the Data

Download the following files from [this link](https://fki.tic.heia-fr.ch/databases/download-the-iam-handwriting-database):

- `data/lines.tgz`
- `data/xml.tgz`

Extract these files into the `data` folder.

### Step 3: Prepare the Inputs for Training

Run the `data-preparation.ipynb` notebook to prepare the inputs for training. This notebook will organize the data and create the necessary input files for the model.

### Step 4: Train the Model

Run the `training.ipynb` notebook to train the model. This notebook will use the prepared data to train a Siamese network for handwriting author verification.

## Directory Structure

Your directory should look like this after extracting the data and running the notebooks:
```
project-root/
│
├── data/
│ ├── authors/
│ ├── lines/
│ ├── xml/
│ ├── tf_inputs/
│ │ ├── dataset_X_train_1.npy
│ │ ├── dataset_X_train_2.npy
│ │ ├── dataset_labels_train.npy
│ │ ├── dataset_X_val_1.npy
│ │ ├── dataset_X_val_2.npy
│ │ └── dataset_labels_val.npy
│ └── .gitkeep
│
├── data-preparation.ipynb
├── training.ipynb
├── .gitignore
└── README.md
```


## Notes

- Make sure that you have all the necessary dependencies installed. You can reference environment.yml to create a conda environent.
- The `data-preparation.ipynb` notebook organizes the data into author-specific folders and generates input files for training.
- The `training.ipynb` notebook trains the Siamese network using the prepared data and saves the trained model.

have fun :)


