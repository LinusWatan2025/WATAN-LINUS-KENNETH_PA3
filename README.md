## OVERVIEW

This repository contains the solutions for **PA3 of the Advanced Computer Programming and Algorithms (ECE2112)** course. The project applies **Pandas** such as loading datasets, subsetting, slicing, indexing, and filtering. Each problem is designed to strengthen data manipulation skills and reinforce the use of Pandas for real-world datasets.

---

## PROBLEM 1

**What it is:**

A program that loads the given CSV file into a Pandas DataFrame named **`cars`** and displays the first and last five rows of the dataset.

**Why it's useful:**

Loading and exploring data is the first step in any data analysis process. This ensures the dataset is correctly imported and gives an initial understanding of the data structure, column names, and values.

**How to get started:**

```python
import pandas as pd

# load CSV file
cars = pd.read_csv('cars.csv')

# display first and last 5 rows
a = cars.head()
b = cars.tail()

combined = pd.concat([a, b], axis=0)

display(cars)
display(combined)
```

**Output:**

<img width="367" height="637" alt="image" src="https://github.com/user-attachments/assets/2b8e0c96-dedd-4d12-93c9-48d3cfa05d1a" />
<img width="741" height="434" alt="image" src="https://github.com/user-attachments/assets/07bbbe8e-5807-4847-af40-8538a8e5b3b3" />


---

## PROBLEM 2

**What it is:**

A set of programs that extract specific information from the **`cars`** DataFrame using **subsetting, slicing, and indexing operations**.

**Why it's useful:**

Efficiently filtering and extracting specific information is a critical skill in data analytics. These exercises practice how to retrieve rows and columns based on conditions, column indices, and logical operators.

**How to get started:**

### a. Display the first five rows with odd-numbered columns (1, 3, 5, 7…).

```python
a = cars.iloc[:5, ::2]
display(a)
```

### b. Display the row that contains the model **Mazda RX4**.

```python
b = cars.loc[cars['Model'] == 'Mazda RX4']
display(b)
```

### c. Display how many cylinders (`cyl`) the car model **Camaro Z28** has.

```python
c = cars.loc[cars['Model'] == 'Camaro Z28', ['Model', 'cyl']]
display(c)
```

### d. Display the cylinders (`cyl`) and gear type (`gear`) for

**Mazda RX4 Wag**, **Ford Pantera L**, and **Honda Civic**.

```python
d = cars.loc[(cars['Model'] == 'Mazda RX4 Wag') | (cars['Model'] == 'Ford Pantera L') | (cars['Model'] == 'Honda Civic'), ['Model', 'cyl', 'gear']]
display(d)
```

**Output:**

**a.**

<img width="460" height="232" alt="image" src="https://github.com/user-attachments/assets/4f1b2765-d7ff-4e5e-a873-b3bbb1e473b2" />

**b.**

<img width="654" height="81" alt="image" src="https://github.com/user-attachments/assets/c4d89188-eee0-4251-88d7-8297bd2b239a" />

**c.**

<img width="186" height="74" alt="image" src="https://github.com/user-attachments/assets/25a7f7a1-1e41-4d6f-8442-7b988777fe62" />

**d.**

<img width="284" height="154" alt="image" src="https://github.com/user-attachments/assets/e9f9175d-75ce-44b7-995d-3c3ec41ddb9a" />


---
