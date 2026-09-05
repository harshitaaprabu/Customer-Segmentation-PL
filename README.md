# Customer Segmentation using K-Means Clustering

This project performs customer segmentation on the **Mall Customers dataset**, using unsupervised machine learning to group customers based on their purchasing behavior. Understanding these segments can help a business tailor marketing strategies, target promotions, and improve customer engagement.

## Dataset

`Mall_Customers.csv` — 200 customer records with the following columns:

| Column | Description |
|---|---|
| CustomerID | Unique identifier for each customer |
| Gender | Male / Female |
| Age | Customer's age |
| Annual Income (k$) | Annual income in thousands of dollars |
| Spending Score (1-100) | Score assigned based on customer behavior and spending nature |

## Project Workflow

1. **Data Loading & Cleaning**
   - Load the dataset with pandas
   - Inspect shape, data types, and check for missing values

2. **Exploratory Data Analysis (EDA)**
   - Distribution plots for Age, Annual Income, and Spending Score
   - Pairwise regression plots between numerical features
   - Gender count plot
   - Scatter plots of Age vs. Income and Income vs. Spending Score, split by gender
   - Violin and swarm plots to compare distributions across genders

3. **K-Means Clustering**
   Clustering is performed on three different feature combinations:
   - **Age vs. Spending Score**
   - **Annual Income vs. Spending Score**
   - **Age, Annual Income, and Spending Score** (3D)

   For each combination:
   - The **Elbow Method** (inertia vs. number of clusters) is used to identify the optimal number of clusters
   - K-Means is fit with the chosen number of clusters
   - Cluster boundaries and centroids are visualized

4. **Visualization**
   - 2D decision-boundary plots with cluster centroids highlighted
   - Interactive 3D scatter plot (Plotly) showing customer clusters across Age, Income, and Spending Score

## Tech Stack

- Python
- pandas, NumPy — data handling
- scikit-learn — K-Means clustering, silhouette score
- Matplotlib, Seaborn — static visualizations
- Plotly — interactive 3D visualization

## Getting Started

### Prerequisites
```bash
pip install numpy pandas matplotlib seaborn plotly scikit-learn
```

### Running the Notebook
1. Clone this repository
   ```bash
   git clone <your-repo-url>
   cd <your-repo-name>
   ```
2. Launch Jupyter Notebook
   ```bash
   jupyter notebook Customer_segmentation_.ipynb
   ```
3. Run the cells in order to reproduce the analysis and visualizations

## Repository Structure

```
.
├── Customer_segmentation_.ipynb   # Main analysis notebook
├── Mall_Customers.csv             # Dataset
└── README.md                      # Project documentation
```

## Results

The analysis identifies distinct customer segments (e.g., high income/low spenders, low income/high spenders, average customers) that can inform targeted marketing and business strategy decisions.

## License

This project is open source and available for personal and educational use.
