import pandas as pd
import matplotlib.pyplot as plt

# Load dataset
df = pd.read_csv('C:/Users/mohan/Downloads/data_salaries/ds_salaries.csv')

# Calculate the correlation matrix
corr = df.corr()

# Create a figure and axis
plt.figure(figsize=(10, 6))

# Create a heatmap using imshow
cax = plt.imshow(corr, cmap='coolwarm', aspect='auto')

# Add color bar
plt.colorbar(cax)

# Set ticks and labels
plt.xticks(range(len(corr.columns)), corr.columns, rotation=45, ha='right')
plt.yticks(range(len(corr.columns)), corr.columns)

# Add title
plt.title('Correlation Heatmap of Data Scientist Salaries', fontsize=16)

plt.show()
