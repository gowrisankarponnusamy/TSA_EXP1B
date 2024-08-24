### NAME: GOWRISANKAR P
### REG NO: 212222230041
### DATE:
# Ex.No: 1B                     CONVERSION OF NON STATIONARY TO STATIONARY DATA
 

### AIM:
To perform regular differncing,seasonal adjustment and log transformatio on international airline passenger data
### ALGORITHM:
1. Import the required packages like pandas and numpy
2. Read the data using the pandas
3. Perform the data preprocessing if needed and apply regular differncing,seasonal adjustment,log transformation.
4. Plot the data according to need, before and after regular differncing,seasonal adjustment,log transformation.
5. Display the overall results.
### PROGRAM:

```
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt

data = pd.read_csv('MentalHealthSurvey.csv')

time_series_data = data['academic_workload ']

log_transformed_data = np.log(time_series_data + 1)  # Adding 1 to avoid log(0)


regular_differenced_data = time_series_data.diff().dropna()

seasonal_differenced_data = time_series_data.diff(1).dropna()

plt.figure(figsize=(14, 10))

LOG TRANSFORMATION:
plt.subplot(4, 1, 2)
plt.plot(log_transformed_data, marker='o', linestyle='-', color='g')
plt.title('Log Transformed Data')
plt.grid(True)

REGULAR DIFFERENCING:
plt.subplot(4, 1, 3)
plt.plot(regular_differenced_data, marker='o', linestyle='-', color='r')
plt.title('Regular Differenced Data')
plt.grid(True)

SEASONAL ADJUSTMENT:
plt.subplot(4, 1, 4)
plt.plot(seasonal_differenced_data, marker='o', linestyle='-', color='m')
plt.title('Seasonal Differenced Data')
plt.grid(True)

plt.tight_layout()
plt.show()
```

### OUTPUT:
LOG TRANSFORMATION:
![image](https://github.com/user-attachments/assets/9bc73f3b-106f-4de4-9a21-a71c4c76fbf0)

REGULAR DIFFERENCING:
![image](https://github.com/user-attachments/assets/334cc97b-5fb2-43c0-bc3f-b0d3f3002588)

SEASONAL ADJUSTMENT:
![image](https://github.com/user-attachments/assets/46f0d953-5f5f-4863-b5a6-e572cd3e8195)

### RESULT:
Thus we have created the python code for the conversion of non stationary to stationary data on international airline passenger
data.
