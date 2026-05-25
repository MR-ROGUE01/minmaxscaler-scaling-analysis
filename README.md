# 🍷 Wine Dataset — Feature Scaling with MinMaxScaler

A beginner-friendly machine learning project demonstrating **data exploration** and **feature scaling** using the Wine dataset. The project walks through EDA, preprocessing, and a visual comparison of data distributions before and after applying `MinMaxScaler`.

---

## 📁 Dataset

**File:** `wine.csv`

The Wine dataset contains results of a chemical analysis of wines grown in a specific region of Italy. This project uses only the first three columns:

| Column | Description |
|--------|-------------|
| `Wine` | Wine class label (1, 2, or 3) |
| `Alcohol` | Alcohol content |
| `Malic.acid` | Malic acid content |

---

## 📌 Project Workflow

### 1. Data Loading & Exploration
- Load `wine.csv` using `pandas`
- Inspect shape, data types, and first few rows
- Subset to the first 3 columns

### 2. Exploratory Data Analysis (EDA)
- **KDE plots** for `Alcohol` and `Malic.acid` distributions
- **Scatter plot** of `Alcohol` vs `Malic.acid`, color-coded by wine class

### 3. Train-Test Split
- Split data into **80% training / 20% test** sets using `train_test_split` with `random_state=0`

### 4. Feature Scaling
- Apply `MinMaxScaler` — fit on training data only, then transform both train and test sets
- Scales features to the **[0, 1]** range

### 5. Visual Comparison
- **Scatter plots** — Before vs. After scaling (training set)
- **KDE plots** — Before vs. After scaling for both features

---

## 🛠️ Tech Stack

- Python 3.x
- `numpy`
- `pandas`
- `matplotlib`
- `seaborn`
- `scikit-learn`

---

## 🚀 Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/your-username/wine-feature-scaling.git
cd wine-feature-scaling
```

### 2. Install dependencies

```bash
pip install numpy pandas matplotlib seaborn scikit-learn
```

### 3. Add the dataset

Place `wine.csv` in the root of the project directory.  
The dataset is publicly available via the [UCI Machine Learning Repository](https://archive.ics.uci.edu/ml/datasets/wine).

### 4. Run the script

```bash
python wine_scaling.py
```

---

## 📊 Sample Visualizations

The script generates four plots:

- KDE plots of raw `Alcohol` and `Malic.acid` distributions
- Scatter plot of features colored by wine class
- Side-by-side scatter: before vs. after scaling
- Side-by-side KDE: before vs. after scaling

---

## 💡 Key Takeaway

MinMaxScaler **preserves the shape** of the original distribution — it only changes the scale, not the spread or relative structure of the data. This is visible in the before/after KDE and scatter plots.

---

## 📄 License

This project is open-source and available under the [MIT License](LICENSE).
