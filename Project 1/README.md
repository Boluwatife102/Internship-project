# Advanced EDA and Feature Engineering

## Project Overview

This project focuses on Exploratory Data Analysis (EDA), data cleaning, outlier treatment, and feature engineering using an e-commerce dataset. The goal was to explore the data, identify data quality issues, and prepare it for further analysis using Python.

## Tools and Libraries

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Jupyter Notebook

## Project Activities

- Explored the dataset and examined its structure.
- Identified and handled missing values.
- Checked for duplicate records.
- Detected outliers using the Interquartile Range (IQR) method.
- Applied Winsorization to cap extreme values without deleting rows.
- Created five new features: Year, Month, DayOfWeek, CartUtilization, and OrderSize.
- Applied One-Hot Encoding to selected categorical variables.

## Outlier Treatment Results

The IQR method identified 8 potential outliers in the `TotalPrice` column. Further investigation showed that these were legitimate high-value orders involving five units of products such as laptops, printers, tablets, chairs, and monitors.

Winsorization was applied using `np.clip()`.

| Measurement | Before Clipping | After Clipping |

|---|---:|---:|
| Maximum TotalPrice | 3,456.40 | 3,330.41 |
| Mean TotalPrice | 1,053.97 | 1,053.64 |
| Number of Rows | 1,200 | 1,200 |

The treatment reduced the influence of extreme values while preserving all 1,200 records.

## Feature Engineering

Five new features were created:

- **Year:** Extracted from the order date.
- **Month:** Extracted from the order date.
- **DayOfWeek:** Identified the day each order was placed.
- **CartUtilization:** Calculated the ratio of Quantity to ItemsInCart.
- **OrderSize:** Categorized orders into Small, Medium, and Large.

## Key Learning Outcomes

This project strengthened my practical skills in:

- Exploratory Data Analysis
- Data Cleaning and Preprocessing
- IQR Outlier Detection and Winsorization
- Feature Engineering
- One-Hot Encoding
- Data Visualization using Python

## Conclusion

This project provided hands-on experience in transforming raw e-commerce data into a structured dataset suitable for further analysis. It improved my understanding of data quality, statistical techniques, and feature preparation using Python.
