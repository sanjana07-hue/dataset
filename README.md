# dataset
import pandas as pd
import random

# Define the number of samples
num_samples = 1000

# Create an empty DataFrame
data = pd.DataFrame()

# Generate sample data for each feature
data['Lead ID'] = range(1, num_samples + 1)
data['Age'] = [random.randint(18, 65) for _ in range(num_samples)]
data['Gender'] = [random.choice(['Male', 'Female', 'Other']) for _ in range(num_samples)]
data['Location'] = [random.choice(['New York', 'Los Angeles', 'Chicago', 'Houston']) for _ in range(num_samples)]
data['Income'] = [random.randint(30000, 120000) for _ in range(num_samples)]
data['Education Level'] = [random.choice(['High School', 'Bachelor', 'Master', 'Ph.D.']) for _ in range(num_samples)]
data['Number of times contacted'] = [random.randint(1, 20) for _ in range(num_samples)]
data['Marketing channel'] = [random.choice(['Email', 'Social Media', 'Phone Call']) for _ in range(num_samples)]
data['Campaign effectiveness'] = [random.uniform(0, 1) for _ in range(num_samples)]
data['Website visits'] = [random.randint(0, 10) for _ in range(num_samples)]
data['Time spent on website'] = [random.uniform(0, 60) for _ in range(num_samples)]
data['Pages viewed'] = [random.randint(1, 10) for _ in range(num_samples)]
data['Previous product interactions'] = [random.choice([0, 1]) for _ in range(num_samples)]

# Generate the binary target variable (Outcome)
data['Outcome'] = [random.choice([0, 1]) for _ in range(num_samples)]

# Save the dataset to a CSV file
data.to_csv('marketing_leads_dataset.csv', index=False)
