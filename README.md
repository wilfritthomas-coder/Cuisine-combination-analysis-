# 🍽️ Cuisine Combination Analysis

> **Task:** Identify the most common cuisine combinations in a restaurant dataset and determine whether certain cuisine pairings tend to achieve higher ratings.

---

## 📁 Project Structure

```
cuisine_combination_analysis/
│
├── data/
│   └── restaurant_dataset.csv          # Source dataset (9,551 restaurant records)
│
├── notebooks/
│   └── cuisine_combination_analysis.ipynb   # Full analysis notebook
│
├── outputs/
│   ├── 01_top15_cuisines.png           # Top 15 most frequent individual cuisines
│   ├── 02_top20_pairs.png              # Top 20 most common cuisine pairs
│   ├── 03_top10_triplets.png           # Top 10 cuisine triplet combinations
│   ├── 04_pairs_by_rating.png          # Cuisine pairs ranked by average rating
│   ├── 05_rating_by_combo_count.png    # Rating distribution by combination count
│   ├── 06_cooccurrence_heatmap.png     # Co-occurrence heatmap (top 10 cuisines)
│   ├── 07_cuisines_by_rating.png       # Top individual cuisines by average rating
│   ├── summary_top15_cuisines.csv
│   ├── summary_top20_pairs.csv
│   ├── summary_top10_triplets.csv
│   ├── summary_pairs_by_rating.csv
│   ├── summary_combo_type_rating.csv
│   └── summary_cuisines_by_rating.csv
│
├── README.md                           # This file
└── task_explanation.txt                # Detailed task explanation
```

---

## 🎯 Objectives

1. **Identify Most Common Cuisine Combinations** — Discover which pairs and triplets of cuisines appear most frequently across restaurants.
2. **Determine Rating Impact** — Analyze whether certain cuisine combinations consistently yield higher aggregate ratings compared to others.

---

## 📊 Dataset Overview

| Attribute        | Detail                        |
|-----------------|-------------------------------|
| Total Records    | 9,551 restaurants             |
| Rated Records    | 7,394 (used for rating analysis) |
| Features         | 21 columns                    |
| Key Columns      | `Cuisines`, `Aggregate rating`, `City`, `Votes` |
| Rating Scale     | 0.0 – 5.0                     |
| Rating Mean      | ~3.47 (across rated records)  |

---

## 🔍 Key Findings

### Most Common Cuisine Pairs
| Rank | Combination                    | Count |
|------|-------------------------------|-------|
| 1    | Chinese + North Indian         | 1,479 |
| 2    | Mughlai + North Indian         | 706   |
| 3    | Continental + North Indian     | 442   |
| 4    | Fast Food + North Indian       | 412   |
| 5    | Chinese + Fast Food            | 378   |

### Most Common Cuisine Triplets
| Rank | Combination                              | Count |
|------|------------------------------------------|-------|
| 1    | Chinese + Mughlai + North Indian         | 314   |
| 2    | Chinese + Continental + North Indian     | 238   |
| 3    | Chinese + North Indian + South Indian    | 225   |

### Top-Rated Cuisine Pairs (min. 5 restaurants)
| Rank | Combination              | Avg Rating |
|------|--------------------------|------------|
| 1    | Asian + Indian           | 4.54       |
| 2    | Sandwich + Seafood       | 4.43       |
| 3    | Bar Food + Brazilian     | 4.41       |
| 4    | Curry + Indian           | 4.40       |
| 5    | European + Mediterranean | 4.18       |

### Rating by Cuisine Count
| Cuisine Count  | Avg Rating | Restaurants |
|---------------|------------|-------------|
| Single Cuisine | 3.40       | 2,224       |
| 2 Cuisines     | 3.39       | 2,737       |
| 3 Cuisines     | 3.49       | 1,603       |
| 4+ Cuisines    | 3.61       | 830         |

> **Insight:** Restaurants offering 4 or more cuisine types tend to receive higher average ratings (3.61) compared to single-cuisine restaurants (3.40), suggesting that variety may positively influence customer perception.

---

## 🛠️ Requirements

```
Python 3.8+
pandas
matplotlib
seaborn
itertools (standard library)
collections (standard library)
```

---

## ▶️ How to Run

1. Open the notebook:
   ```bash
   jupyter notebook notebooks/cuisine_combination_analysis.ipynb
   ```

2. Run all cells sequentially (Kernel → Restart & Run All)

3. All charts and CSV summaries will be saved automatically to `outputs/`

---

## 📈 Visualizations Produced

| # | Chart | Description |
|---|-------|-------------|
| 01 | Top 15 Cuisines | Frequency of individual cuisine types |
| 02 | Top 20 Pairs | Most common two-cuisine combinations |
| 03 | Top 10 Triplets | Most common three-cuisine combinations |
| 04 | Pairs by Rating | Highest-rated cuisine pair combinations |
| 05 | Rating by Count | How number of cuisines affects ratings |
| 06 | Co-occurrence Heatmap | Cuisine pairing frequency matrix |
| 07 | Cuisines by Rating | Highest-rated individual cuisine types |

---

*This analysis was conducted as part of a data analytics internship task.*
