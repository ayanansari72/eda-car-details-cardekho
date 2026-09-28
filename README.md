# 🚗 Car Dekho – Exploratory Data Analysis

Exploratory data analysis (EDA) of used-car listings from **CarDekho**, using
Python, Pandas, Seaborn, Matplotlib and Plotly. The notebook explores which
brands, fuel types, transmissions, seller types and model years dominate the
used-car market in the dataset.

## 📂 Repository Structure

​```
car-dekho-eda/
├── eda-car-data-analysis.ipynb   # Main analysis notebook
├── CAR DETAILS FROM CAR DEKHO.csv  # Dataset (add here)
└── README.md
​```

## 📊 Dataset

- **File:** `CAR DETAILS FROM CAR DEKHO.csv`
- **Rows / Columns:** 4,340 / 8
- **Missing values:** none

| Column          | Description                                           |
|-----------------|-------------------------------------------------------|
| `name`          | Car brand and model                                   |
| `year`          | Year of manufacture (1992–2020)                       |
| `selling_price` | Listed selling price (INR)                            |
| `km_driven`     | Kilometres driven                                     |
| `fuel`          | Petrol, Diesel, CNG, LPG, Electric                    |
| `seller_type`   | Individual, Dealer, Trustmark Dealer                  |
| `transmission`  | Manual or Automatic                                   |
| `owner`         | First, Second, Third, Fourth & Above, Test Drive Car  |

An additional feature `name_2` (car brand) is derived from the first word of `name`.

## 🔍 What the Notebook Does

1. **Data inspection** – `head`, `info`, `describe`, `shape`, null check
2. **Feature engineering** – extracts the brand name from the car name
3. **Univariate analysis** – count plots, pie charts and a word cloud for brand, year, fuel, seller type, transmission and owner
4. **Bivariate / multivariate analysis**
   - Year distribution by transmission
   - Fuel vs. year violin plot
   - Brand vs. transmission and brand vs. owner cross-tabs
   - Kilometres driven by brand (bar and box plots)
   - Correlation heatmap of numeric features
5. **Interactive Plotly charts** – treemap (transmission → fuel → brand by median price), sunburst charts (year → brand) and a strip plot

## 💡 Key Findings

- **Maruti** is the most listed brand (1,280 cars), followed by **Hyundai** (821).
- **Manual** cars dominate (~90%, 3,892 of 4,340).
- **Diesel** and **Petrol** account for nearly all listings (~99%).
- Most cars are **first-owner** (2,832), followed by second-owner (1,106).
- About **75%** of cars are sold by **individuals** (3,244).
- **2017** has the most listings (466 cars).

## 🛠️ Tech Stack

- Python 3
- Pandas, NumPy
- Matplotlib, Seaborn
- Plotly
- WordCloud

## 🚀 How to Run

​```bash
# 1. Clone the repository
git clone https://github.com/<your-username>/car-dekho-eda.git
cd car-dekho-eda

# 2. Install dependencies
pip install numpy pandas seaborn matplotlib plotly wordcloud jupyter

# 3. Launch the notebook
jupyter notebook eda-car-data-analysis.ipynb
​```

Make sure `CAR DETAILS FROM CAR DEKHO.csv` is in the same folder as the notebook.

## 📈 Possible Future Work

- Build a price-prediction model (regression)
- Add outlier handling for `selling_price` and `km_driven`
- Add a `car_age` feature and analyse depreciation

## 📝 License

This project is licensed under the MIT License.
