# 📱 Google Play Store App Market & User Ratings Analysis

An in-depth Exploratory Data Analysis of the Android app market ecosystem, examining app categories, user ratings, download volumes, pricing strategies, and content ratings.

---

## 📌 Project Overview

With millions of applications on mobile marketplaces, understanding the determinants of app success — user ratings, review volume, installation scale, and monetization models — is essential for product managers and developers. This project performs end-to-end data cleaning and exploratory analysis on over 10,000 Play Store applications to evaluate market dynamics, category competition, and rating distributions.

---

## 📊 Dataset Overview

The dataset (`googleplaystore.csv`) captures key app metrics:

* **Identity & Categorization:** `App` name, `Category` (Family, Game, Tools, Productivity, etc.), `Genres`.
* **User Feedback & Traction:** `Rating` (1.0 to 5.0 scale), `Reviews` (total user review count), `Installs` (download tiers).
* **Technical & Operational:** `Size` (KB/MB payload), `Current Ver`, `Android Ver` compatibility, `Last Updated`.
* **Monetization & Compliance:** `Type` (`Free` vs. `Paid`), `Price` (USD), `Content Rating` (Everyone, Teen, Mature 17+).

---

## 🧹 Data Cleaning & Preprocessing

The raw dataset presents several real-world data challenges addressed in the notebook:
* **String Sanitization:** Stripped non-numeric characters from `Installs` (`+`, `,`) and converted to numeric integers.
* **Price Standardization:** Removed currency symbols (`$`) and parsed values into continuous floating-point numbers.
* **Review Parsing:** Handled corrupt review rows and cast to integer format.
* **Size Conversion:** Parsed variable file size notation (`M` for megabytes, `k` for kilobytes) into unified numeric representations.
* **Missing Value Imputation:** Addressed null values across user ratings and operational metadata.

---

## 🔍 Key Findings & Market Insights

1. **Category Dominance:**
   * **Family**, **Game**, and **Tools** account for the highest volume of available applications.
   * In terms of aggregate download volume, **Communication**, **Social**, and **Video Players** capture dominant install numbers.

2. **Rating Distribution:**
   * Average user rating clusters around **4.17**, indicating a positive skew in voluntary user reviews.
   * Free apps demonstrate a broader dispersion in ratings, whereas Paid applications tend to maintain slightly higher and tighter rating medians due to self-selecting, committed user bases.

3. **Monetization Analysis:**
   * Over 90% of Play Store applications follow the Free (ad-supported/in-app purchase) model.
   * Paid applications dominate specific niches such as Personalization, Medical, and specialized productivity tools.

---

## 📈 Visualizations in the Notebook

* **Category Distribution:** Count plots tracking total app volume across all 33 Play Store categories.
* **Market Share Breakdown:** Pie chart highlighting the top 5 most saturated app categories.
* **Rating Distributions by Type:** FacetGrid comparative histograms contrasting Free vs. Paid app rating distributions.
* **Correlation Heatmap:** Numeric correlation matrix evaluating relationships between App Size, Ratings, Reviews, and Installs.
* **Top Performers:** Bar charts ranking the most reviewed and installed applications.

---

## 🛠️ Tech Stack

* **Language:** Python 3.x
* **Libraries:** `pandas`, `numpy`, `matplotlib`, `seaborn`, `jupyter`
* **Dataset:** `googleplaystore.csv`

---

## 🚀 Getting Started

### 1. Clone the Repository
```bash
git clone https://github.com/Zelarq/playstore-apps-analysis.git
cd playstore-apps-analysis
```

### 2. Set Up Virtual Environment
```bash
python -m venv venv
# On Windows:
venv\Scripts\activate
# On macOS/Linux:
source venv/bin/activate
```

### 3. Install Dependencies
```bash
pip install -r requirements.txt
```

### 4. Launch Jupyter Notebook
```bash
jupyter notebook playstore_project.ipynb
```

---

## 👤 Author

* **Sayanth N K**
* GitHub: [@Zelarq](https://github.com/Zelarq)
* Email: [sayanthnk32@gmail.com](mailto:sayanthnk32@gmail.com)
