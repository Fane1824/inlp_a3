# Word Embedding Training and Evaluation

## 1. Final Submission Contents

The final submission contains the following files:

### Training Scripts
- **svd.py**: Trains word embeddings using the Singular Value Decomposition (SVD) method and saves the word vectors.
- **skipgram.py**: Trains word embeddings using the Skip-gram method (with negative sampling) and saves the word vectors.
- **cbow.py**: Trains word embeddings using the Continuous Bag of Words (CBOW) method (with negative sampling) and saves the word vectors.

### Saved Word Vectors
- **svd.pt**: Saved word vectors for the entire vocabulary trained using SVD.
- **skipgram.pt**: Saved word vectors for the entire vocabulary trained using Skip-gram (with negative sampling).
- **cbow.pt**: Saved word vectors for the entire vocabulary trained using CBOW (with negative sampling).

### Additional Files
- **results/**: A folder containing plots as referenced in the report.
- **wordsim.py**: Contains the code for evaluating word similarity using the WordSim-353 dataset.
- **helper.py**: Contains helper functions for loading and processing the dataset.

---

## 2. Training the Embeddings

To train the word embeddings using different methods, run the following scripts:
```sh
python3 svd.py
python3 skipgram.py
python3 cbow.py
```
Each script generates a corresponding `.pt` file containing the trained word vectors.

---

## 3. Evaluating on WordSim-353

### Preparation
1. Place the **WordSim-353 dataset** file (e.g., `WordSim353 Crowd.csv`) in the project folder.
2. This file can be found in the assignment question document.

### Running Evaluation
To evaluate a trained word embedding model, use the following command:
```sh
python3 wordsim.py --model <path_to_model.pt> --wordsim "WordSim353 Crowd.csv" --plot 
```
Replace `<path_to_model.pt>` with the specific trained model file (e.g., `svd.pt`, `skipgram.pt`, or `cbow.pt`). This script:
- Computes the **Spearman correlation** between the trained embeddings and the WordSim-353 dataset.
- Produces a **scatter plot** saved in the `results/` folder.

---

## Dependencies
Ensure you have the required dependencies installed before running the scripts:
```sh
pip install numpy torch matplotlib pandas
```

--- 

## Models

https://drive.google.com/drive/folders/1_8C77nr22T_GLaVESr5VaKIh1b_S_XMl?usp=sharing


