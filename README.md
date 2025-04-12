## NAME : NAVEEN KUMAR T
## REG NO : 212223220067
### EX4 Implementation of Cluster and Visitor Segmentation for Navigation patterns
### DATE: 12:04:2025
### AIM: To implement Cluster and Visitor Segmentation for Navigation patterns in Python.
### Description:
<div align= "justify">Cluster visitor segmentation refers to the process of grouping or categorizing visitors to a website, 
  application, or physical location into distinct clusters or segments based on various characteristics or behaviors they exhibit. 
  This segmentation allows businesses or organizations to better understand their audience and tailor their strategies, marketing efforts, 
  or services to meet the specific needs and preferences of each cluster.</div>
  
### Procedure:
1) Read the CSV file: Use pd.read_csv to load the CSV file into a pandas DataFrame.
2) Define Age Groups by creating a dictionary containing age group conditions using Boolean conditions.
3) Segment Visitors by iterating through the dictionary and filter the visitors into respective age groups.
4) Visualize the result using matplotlib.

### Program:
```python code
data = {
    'VisitorID': [1, 2, 3, 4, 5, 6],
    'Age': [18, 24, 35, 45, 60, 70],
    'Gender': ['Male', 'Female', 'Male', 'Female', 'Male', 'Female']
}

# Convert to DataFrame
df = pd.DataFrame(data)

# Perform segmentation based on age groups
def segment_age(age):
    if age < 20:
        return 'Teen'
    elif age < 30:
        return 'Young Adult'
    elif age < 50:
        return 'Adult'
    elif age < 65:
        return 'Middle Aged'
    else:
        return 'Senior'

# Apply segmentation function
df['AgeGroup'] = df['Age'].apply(segment_age)

# Show the segmented DataFrame
print(df)
```
### Output:
![Screenshot 2025-04-12 085649](https://github.com/user-attachments/assets/1a04f8f9-00bc-4684-87a2-c1ce67458a44)

## Visualization:
``` python code
import pandas as pd
import matplotlib.pyplot as plt

# Sample data
data = {
    'VisitorID': [1, 2, 3, 4, 5, 6, 7, 8, 9, 10],
    'Age': [16, 22, 29, 35, 41, 55, 61, 68, 75, 83],
    'Gender': ['M', 'F', 'M', 'F', 'M', 'F', 'M', 'F', 'M', 'F']
}

# Create DataFrame
df = pd.DataFrame(data)

# Define age group function
def segment_age(age):
    if age < 20:
        return 'Teen'
    elif age < 30:
        return 'Young Adult'
    elif age < 50:
        return 'Adult'
    elif age < 65:
        return 'Middle Aged'
    else:
        return 'Senior'

# Apply segmentation
df['AgeGroup'] = df['Age'].apply(segment_age)

# Create a list to store counts of visitors in each age group
age_group_labels = ['Teen', 'Young Adult', 'Adult', 'Middle Aged', 'Senior']

#  Count visitors in each age group
visitor_counts = df['AgeGroup'].value_counts().reindex(age_group_labels, fill_value=0).tolist()

# Define age group labels and plot a bar chart
plt.figure(figsize=(8, 6))
plt.bar(age_group_labels, visitor_counts, color='skyblue')
plt.xlabel('Age Groups')
plt.ylabel('Number of Visitors')
plt.title('Visitor Distribution Across Age Groups')
plt.show()
```
### Output:
![Screenshot 2025-04-12 085736](https://github.com/user-attachments/assets/ea532bf8-7664-4b91-89c0-2dc3df08071f)


### Result:
Hence Cluster and Visitor Segmentation for Navigation attern in pythonis implemented 
