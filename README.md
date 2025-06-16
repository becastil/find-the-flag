# 🇺🇳 Find the Flag: Decision Tree Classification

This project uses a decision tree classifier to predict which **landmass (continent)** a flag comes from based on its features (colors and shapes).

---

## 📂 Dataset

Dataset: `flags.csv`  
Source: [UCI Machine Learning Repository](https://archive.ics.uci.edu/dataset/40/flags)

---

## ✅ Step-by-Step Instructions (based on Codecademy's Find the Flag project)

### Investigate the Data

1. Load the data into a variable called `flags` using `pd.read_csv("flags.csv", header=0)`
2. Print the column names with `flags.columns` and preview the first few rows with `flags.head()`
3. Refer to the dataset legend to understand what each number means — e.g., Andorra has `"Landmass" = 3`, which means Europe

### Creating Your Data and Labels

4. Create a variable called `labels` and set it equal to `flags[["Landmass"]]`
5. Create a variable called `data` with only the following columns:  
   `"Red", "Green", "Blue", "Gold", "White", "Black", "Orange"`
6. Split `data` and `labels` into `train_data`, `test_data`, `train_labels`, and `test_labels` using `train_test_split()` with `random_state=1`

### Make and Test the Model

7. Create a `DecisionTreeClassifier` called `tree` with `random_state=1`
8. Call `.fit(train_data, train_labels)` to train the tree
9. Call `.score(test_data, test_labels)` and print the result to evaluate accuracy

### Tuning the Model

10. Use a `for` loop to test how model accuracy changes as you vary `max_depth` from 1 to 20
11. Store all accuracy scores in a list called `scores` using `.append()`
12. Plot the results using `plt.plot(range(1, 21), scores)` and `plt.show()`

### Add More Features

13. Add more features to `data`:  
    `"Circles", "Crosses", "Saltires", "Quarters", "Sunstars", "Crescent", "Triangle"`  
    Re-split the data, retrain the model, and re-plot the accuracy

### Explore on Your Own

14. Try variations:
    - Predict `"Language"` instead of `"Landmass"`
    - Try other feature sets
    - Tune other hyperparameters like `max_leaf_nodes`
