# Principal Component Analysis for Baseball Player Clustering
## Technical doc

## Table of Contents
1. [Project Overview](#1-project-overview)
2. [Theoretical Background](#2-theoretical-background)
3. [Data Structure](#3-data-structure)
4. [Implementation Details](#4-implementation-details)
5. [Function Reference](#5-function-reference)
6. [Pandas Operations Guide](#6-pandas-operations-guide)
7. [Mathematical Details](#7-mathematical-details)

## 1. Project Overview

### Key Features
- Dimensionality reduction using PCA
- Player similarity clustering
- Year-over-year variance analysis
- Comprehensive player comparison reporting

## 2. Theoretical Background

### Principal Component Analysis (PCA)
PCA is a dimensionality reduction technique that transforms high-dimensional data into a new coordinate system where the axes (principal components) are ordered by the amount of variance they explain.

#### Key Concepts
- **Singular Value Decomposition (SVD)**: The mathematical foundation used to compute principal components
- **Mean Centering**: Data preprocessing step where the mean is subtracted from each feature
- **Variance Explained**: The proportion of total variance captured by each principal component

### Mathematical Foundation
The SVD decomposition is expressed as:
```
A = USV^T
```
where:
- A: Mean-centered data matrix
- U: Left singular vectors (principal component directions)
- S: Singular values (square root of eigenvalues)
- V: Right singular vectors

## 3. Data Structure

### Input Data (`fgswing.csv`)
The analysis uses six key batting metrics:
1. **O-Swing%**: Percentage of swings at pitches outside the strike zone
2. **Z-Swing%**: Percentage of swings at pitches inside the strike zone
3. **O-Contact%**: Contact rate on swings at pitches outside the strike zone
4. **Z-Contact%**: Contact rate on swings at pitches inside the strike zone
5. **Soft%**: Percentage of soft contact
6. **Hard%**: Percentage of hard contact
### DataFrame Structure
```python
columns = ['Name', 'Team', 'Season', 'O-Swing%', 'Z-Swing%', 'O-Contact%', 
           'Z-Contact%', 'Soft%', 'Hard%']
```
## 4. Implementation Details
### Key Functions Overview
1. `data_to_svd(year)`
   - Performs SVD on year-specific data
   - Returns U, S, Vh matrices

2. `make_pcdf()`
   - Creates principal component DataFrame
   - Computes weighted principal components for each player

3. `make_vardf()`
   - Calculates variance explained by principal components
   - Tracks changes in variance across years

4. `get_comps(player, year)`
   - Finds similar players using PCA coordinates
   - Returns top 3 most similar players

5. `cluster_report(year)`
   - Generates comprehensive similarity report
   - Maps all players to their closest comparisons

## 5. Function Reference

### data_to_svd(year)
```python
def data_to_svd(year):
    """
    Parameters:
    year (int): Season year (2021-2024)
    
    Returns:
    tuple: (U, S, Vh) matrices from SVD
    """
```

### get_comps(player, year)
```python
def get_comps(player, year):
    """
    Parameters:
    player (str): Player name
    year (int): Season year
    
    Returns:
    list: Three most similar players
    """
```

## 6. Pandas Operations Guide

### Key DataFrame Operations

1. **Filtering Data**
```python
year_data = sdf[sdf['Season'] == year]
```

2. **Column Selection**
```python
A = year_data[swing_cols]
```

3. **Index Reset**
```python
year_data = year_data.reset_index(drop=True)
```

4. **Value Assignment**
```python
rep_df.loc[index, ['Comp1', 'Comp2', 'Comp3']] = comps
```

### Common Patterns

1. **DataFrame Creation**
```python
pd.DataFrame({
    'Name': names,
    'Season': year
})
```

2. **Sorting**
```python
comp_df = comp_df.sort_values('distance')
```

## 7. Mathematical Details

### Variance Calculation
The variance explained by principal components is calculated as:

1. Square singular values: `S^2`
2. Calculate total variance: `total_var = sum(S^2)`
3. Compute cumulative sums: `cumsum(S^2[:5])`
4. Convert to percentages: `(cumsum / total_var) * 100`

### Distance Calculation
Player similarity is computed using Euclidean distance in the first three principal components:
```python
distances = np.sqrt(np.sum((U_3 - player_coords)**2, axis=1))
```

### Data Preprocessing
1. Filter by year
2. Extract swing columns
3. Mean center the data:
```python
A = A - np.mean(A, axis=0)
```

## Best Practices

1. Always copy DataFrames before modification:
```python
sdf = global_sdf.copy()
```

2. Reset indices after filtering:
```python
year_data = year_data.reset_index(drop=True)
```

3. Use proper column names in sorting:
```python
df = df.sort_values('column_name', ascending=True)
```

4. Handle index alignment carefully when assigning values:
```python
df.loc[index, columns] = values
```

