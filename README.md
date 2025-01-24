# Step-by-Step Markdown Documentation
# 1. Introduction
The notebook starts with an introduction, setting the context for analyzing the Boston Housing dataset.
2. Libraries Used
The following libraries are imported, and their purposes are explained:
pandas (pd): For data manipulation and analysis.
NumPy (np): For numerical computations.
Matplotlib.pyplot (plt): For data visualization.
Seaborn (sns): For statistical graphics.
3. Loading the Dataset
The dataset is loaded into a pandas DataFrame using pd.read_csv.
df = pd.read_csv('/content/boston.csv')
4. Viewing the Data
The structure and content of the DataFrame are displayed.
df
5. Correlation Analysis
The correlation between the number of rooms (RM) and the median value (MEDV) is calculated and displayed.
correlation = df['RM'].corr(df['MEDV'])
correlation
6. Highest Correlation with Median Value
The variable with the highest correlation to MEDV (excluding MEDV itself) is identified.
correlations = df.corr()['MEDV'].abs().sort_values(ascending=False)
highest_correlation_variable = correlations.index[1]correlations
8. Distribution of Pupil-Teacher Ratio
A histogram is plotted to visualize the distribution of the pupil-teacher ratio by town.
plt.hist(df['PTRATIO'])
plt.xlabel('Pupil-Teacher Ratio')
plt.ylabel('Frequency')
plt.title('Distribution of Pupil-Teacher Ratio by Town')
plt.show()
9. Average Age of Homes
The average age of homes is calculated.
average_age = df['AGE'].mean()
average_age
10. Town with Highest Median Value
The town with the highest median value is identified, and its corresponding row in the dataset is displayed.
index_of_max_medv = df['MEDV'].idxmax()
row_with_highest_medv = df.loc[index_of_max_medv]
row_with_highest_medv
