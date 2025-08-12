# Ex.No: 01A PLOT A TIME SERIES DATA
###  Date: 

# AIM:
To Develop a python program to Plot a time series data (population/ market price of a commodity
/temperature.
# ALGORITHM:
1. Import the required packages like pandas and matplot
2. Read the dataset using the pandas
3. Calculate the mean for the respective column.
4. Plot the data according to need and can be altered monthly, or yearly.
5. Display the graph.

# DATASET:
https://www.kaggle.com/datasets/wasiqaliyasir/breast-cancer-dataset/code
## NAME: MOHAMED HAMEEM SAJITH J
## REG: 212223240090
# PROGRAM:
```
import pandas as pd
import matplotlib.pyplot as plt

try:
    file_path = 'Breast_cancer_dataset.csv'
    data = pd.read_csv(file_path)

    # 3: Create a figure and axes for the plot
    fig, ax = plt.subplots(figsize=(10, 7))

    # 4: Separate data based on diagnosis
    malignant = data[data['diagnosis'] == 'M']
    benign = data[data['diagnosis'] == 'B']

    # 5: Plot data for malignant cases
    ax.scatter(malignant['radius_mean'], malignant['texture_mean'], 
               color='red', label='Malignant', alpha=0.6)

    # 6: Plot data for benign cases
    ax.scatter(benign['radius_mean'], benign['texture_mean'], 
               color='blue', label='Benign', alpha=0.6)

    # 7: Customize the plot with title and labels
    ax.set_title('Tumor Radius vs. Texture by Diagnosis', fontsize=16)
    ax.set_xlabel('Mean Radius of Tumor', fontsize=12)
    ax.set_ylabel('Mean Texture of Tumor', fontsize=12)

    # 8: Add a legend
    ax.legend()

    # 9: Add a grid
    ax.grid(True)

    # 10: Display the plot
    plt.show()

except FileNotFoundError:
    print(f"Error: The file '{file_path}' was not found.")
except KeyError as e:
    print(f"Error: A required column {e} was not found in the CSV file.")


```



# OUTPUT:

<img width="845" height="630" alt="image" src="https://github.com/user-attachments/assets/29da2120-a242-428f-805a-acf7be68f4b9" />





# RESULT:
Thus we have created the python code for plotting the time series of given data.
