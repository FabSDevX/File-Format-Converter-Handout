# File Format Converter Handout
The objective of this project is to develop solutions based on the design provided. In this case, the source data was obtained in the form of CSV files from a MySQL DB.

To improve the efficiency of our data engineering pipelines, we need to convert these CSV files into JSON files, since JSON is better to use in downstream applications than CSV files. The scope of this project involves converting CSV files into JSON files.

### Data Model Details
![image](https://github.com/user-attachments/assets/77882e8f-a9bb-462e-9715-0bbb3fdb0de8)

### Design
![image](https://github.com/user-attachments/assets/beead5ef-4fc2-4fa1-82a4-f4039bd8c8b4)

### Setup Instructions
1. Setup the Project Using VSCode
2. Make sure you have set up a virtual environment (creating venv, requirements.txt, etc.,) and installed dependencies for the project.
3. It is essential that you deploy the application with the core logic.
4. Run the project after setting all the environment variables.
5. Take appropriate steps to handle the exception

### Validation Steps

* You should check whether the data in the files has been converted properly.
* Make sure the target folder has been created and populated with JSON files and confirm that the schema structure was accurately reflected from the CSV file. (Hint: Refer to schemas.json)
* Take the count of records in the CSV files and compare it to the number of records in the JSON files.
``` Python
import pandas as pd
# ###### Read orders JSON File using PANDAS
orders_data_json= pd.read_json(
    'data/retail_db/orders_json/part-00000',
    lines=True
)
# To find count of rows
orders_data_json.count()
# ###### Read order_items JSON File using PANDAS
order_items_data_json= pd.read_json(
    'data/retail_db/order_items_json/part-00000',
    lines=True
)
# To find count of rows
order_items_data_json.count()
```

### Technologies Used
* Programming Language – Python
* Pandas – For Converting CSV to Dataframe and then Dataframe into JSON.
