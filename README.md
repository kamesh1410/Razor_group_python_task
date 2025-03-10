# Razor Group Python Task - E-commerce Seller Analysis

## Project Overview
This project aims to analyze e-commerce seller data from Amazon’s Garden category to identify **promising acquisition targets** for Razor Group. The task involves data cleaning, parsing unstructured text, and developing selection criteria to identify top-performing sellers.

## Dataset Description
The dataset contains seller information, including:  
- `sellerproductcount` – Total number of products listed.  
- `sellerratings` – Positive rating percentage and total ratings.  
- `sellerdetails` – Contact details like email and phone numbers.  
- `businessaddress` – Seller’s country of registration.  
- `Hero Product 1 #ratings` & `Hero Product 2 #ratings` – Number of ratings for top-performing products.  

## Steps Followed
### 1. Data Loading
- Loaded the `.xlsx` file using Pandas.  
- Displayed the data structure using `.info()` and `.describe()` to understand its characteristics.  

### 2. Data Cleaning
- Extracted product counts using regex from `sellerproductcount`.  
- Extracted positive ratings and total number of ratings from `sellerratings`.  
- Extracted email addresses and phone numbers from `sellerdetails`.  
- Parsed country codes from `businessaddress` and excluded Chinese sellers (`CN`).  
- Converted `Hero Product 1 #ratings` and `Hero Product 2 #ratings` to numeric values.  
- Filled missing values with appropriate defaults:  
  - **Numerical Columns** → Filled with `0`.  
  - **Email & Phone** → Filled with `'Not Available'`.  
  - **Country** → Filled with `'Unknown'`.  

### 3. Identifying Promising Sellers
Promising sellers were identified using the following criteria:  
✅ Product count > 10,000  
✅ Positive rating percentage > 80%  
✅ Total rating count > 50  
✅ Hero Product 1 and Hero Product 2 ratings > 500  
✅ Sellers located in **US** or **Germany**  

### 4. Data Visualization
- **Bar Chart:** Number of promising sellers by country.  
- **Scatter Plot:** Product count vs. positive rating percentage.  

### 5. Insights Summary
- Total number of promising sellers identified.  
- Country with the most promising sellers.  
- Average product count and positive rating percentage among promising sellers.  

## Code Execution
1. **Install Dependencies**  

2. **Run the Python Script**  

3. **Generated Files**  
- `Cleaned_Data.xlsx` — Contains the cleaned dataset.  
- `Promising_Sellers.xlsx` — Final list of identified promising sellers.  

## Insights Summary
- Total Promising Sellers Identified: `<Count>`  
- Top Country with Most Promising Sellers: `<Country>`  
- Average Product Count of Promising Sellers: `<Value>`  
- Average Positive Rating %: `<Value>%`  

## Technologies Used
- **Python**  
- **Pandas**  
- **Matplotlib**  
- **Seaborn**  

## Contact Information
For any questions or clarifications, feel free to reach out.
