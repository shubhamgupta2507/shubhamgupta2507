# importing pandas module
import pandas as pd

# making data frame
df = pd.read_csv("C:\\Users\\shiva_\\OneDrive\\Documents\\excle data.csv")

print(df)

# import module
import pandas as pd

# assign data
dataFrame = pd.DataFrame({'Name': [' RACHEL ', ' MONICA ', ' PHOEBE ',
                                   ' ROSS ', 'CHANDLER', ' JOEY '],

                          'Age': [30, 35, 37, 33, 34, 30],

                          'Salary': [100000, 93000, 88000, 120000, 94000, 95000],

                          'JOB': ['DESIGNER', 'CHEF', 'MASUS', 'PALENTOLOGY',
                                  'IT', 'ARTIST']})
# filter dataframe
display(
    dataFrame.loc[(dataFrame['Salary'] >= 100000) & (dataFrame['Age'] < 40) & (dataFrame['JOB'].str.startswith('D')),
                  ['Name', 'JOB']])


import pandas as pd

# create a sample DataFrame
data = {'Name': ['Alice', 'Bob', 'Charlie', 'David'],
        'Department': ['HR', 'Marketing', 'Marketing', 'IT'],
        'Salary': [50000, 60000, 55000, 70000]}

df = pd.DataFrame(data)

# display the original DataFrame
print("Original DataFrame:")
print(df)
print("\n")

# use logical operators to filter
filtered_df = df[df.Salary > 55000]

# display the filtered DataFrame
print("Filtered DataFrame:")
print(filtered_df)

import pandas as pd

# create a sample DataFrame
data = {'Name': ['Alice', 'Bob', 'Charlie', 'David'],
        'Department': ['HR', 'Marketing', 'Marketing', 'IT'],
        'Salary': [50000, 60000, 55000, 70000]}

df = pd.DataFrame(data)

# display the original DataFrame
print("Original DataFrame:")
print(df)
print("\n")

# use query method
filtered_df = df.query('Salary > 55000 and Department == "Marketing"')

# display the filtered DataFrame
print("Filtered DataFrame:")
print(filtered_df)
