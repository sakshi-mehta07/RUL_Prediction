
# RUL Prediction (NASA C-MAPSS)

This project uses deep learning to predict how much life is left in a jet engine before it breaks down, using NASA's C-MAPSS dataset.

## Repository Structure

- All the code files, including preprocessing and the models, are inside the `code` folder.
- The raw text data files from the C-MAPSS dataset are stored in the `data` folder.
- When you run the preprocessing notebook correctly (after fixing the file paths), it will create a new folder called `tensors`. This folder will store the cleaned and processed data. There will also be a `transformer` folder inside `tensors` that holds data specifically prepared for the Transformer model.

## Run the Code

### 1. Clone the Repository
### 2: Run Preprocessing First on Raw Data
Open and run the notebook:
```
code/Preprocessing_data_augmentation.ipynb
```
This notebook loads the raw data, cleans it, applies data augmentation, and saves the final processed data in the `tensors` folder.
#### Edit File Paths
Inside the notebook, there is the following line that sets the file path to access the data:
```python
file_path = '/content/drive/MyDrive/Colab Notebooks/I Learn Deep'
```
This file path needs to be changed to match your computer or colab setup
If running locally:
```python
file_path = '..'
```
If using Google Colab:
1. Upload the project folder to your Google Drive.
2. Then update the path like this:
```python
file_path = '/content/drive/MyDrive/your-folder-name/2025-projects-i-learn-deep'
```
Make sure the `data` folder contains all the `.txt` files before you run it.

Please create the folder structure as follows:
```
file_path/
├── data/
└── results/
└── tensors/
    └── transformer/
```

### 3: Train the Models
You can now open any of the following notebooks in the `code` folder to train a model:
- `Autoencoder-BiLSTM.ipynb`
- `HDNN_Model.ipynb`
- `ResCNN.ipynb`
- `Transformer_architecture.ipynb`
- `Ensemble model.ipynb`
Each notebook loads the data that was saved during preprocessing. Inside each notebook, look for this line:
```python
base_path = '/content/drive/MyDrive/Colab Notebooks/I Learn Deep/tensors'
```
Update this path the same way as earlier so the notebook can access the processed data in the tensors folder. Make sure the path has `/tensors` at the end.

Once paths are set correctly, you can run any model notebook to train and evaluate predictions on the processed data.
