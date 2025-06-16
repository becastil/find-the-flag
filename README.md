# find-the-flag

# 🇺🇳 Find the Flag: Decision Tree Classification Project

This project uses a decision tree to predict **which continent a country's flag is from** based on its colors and shapes. The dataset comes from the [UCI Machine Learning Repository](https://archive.ics.uci.edu/dataset/40/flags).

---

## 📂 Dataset

File: `flags.csv`

Each row represents a country's flag with features including:
- **Colors** (`Red`, `Green`, `Blue`, `Gold`, etc.)
- **Shapes** (`Circles`, `Crosses`, `Sunstars`, etc.)
- **Target label**: `Landmass` (continent)

Refer to the dataset legend for meaning of values:  
🔗 https://archive.ics.uci.edu/dataset/40/flags

---

## 🧠 Goal

Use a **Decision Tree Classifier** to:
- Predict the continent (`Landmass`) based on flag features
- Evaluate accuracy at different tree depths
- Visualize how depth affects model performance

---

## 🪜 Steps

1. **Load the data** using `pandas.read_csv()`
2. **Preview columns and rows** with `.columns` and `.head()`
3. **Extract labels** from the `"Landmass"` column
4. **Select features** (flag colors and shapes)
5. **Split the data** into training and test sets using `train_test_split`
6. **Train a decision tree** using `DecisionTreeClassifier`
7. **Evaluate accuracy** with `.score()`
8. **Tune max_depth** of the tree using a loop (depths 1 to 20)
9. **Visualize performance** with `matplotlib.pyplot`
10. **Add shape-based features** and repeat to improve accuracy

---

## 📈 Example Output

```python
Depth 3: 47.62%
Depth 4: 52.38%
...
