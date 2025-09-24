# order-priority-validation
Excel solution for order priority data validation task using VLOOKUP + IFNA
You are given two sheets containing Order and its priority details, but there were some issues while capturing the data, your job is to identify them using
Follow the steps described below.

Step 1: Find the Order Priority from the Orders sheet and fill in the blank column Order Priority in the Priority sheet using a Lookup function.

Step 2: For the error in the data capturing process all Order_IDs may not be present in our records, Please handle them using the IFNA function, and if the name is not found display  "Not Found" 
 
Tasks
1.
Fill up the column Order Priority by using VLOOKUP function and wrapping it by IFNA
# Order Priority Data Validation Solution

## 📌 Problem Statement
We were given two sheets (`Orders` and `Priority`) with some missing or mismatched data.  
The task was to validate and fill in the **Order Priority** column in the `Priority` sheet.

### Requirements
1. Retrieve `Order Priority` from the **Orders** sheet and fill missing values in the **Priority** sheet.  
2. Handle cases where an `Order_ID` does not exist in the `Orders` sheet by displaying **"Not Found"**.  

---

## 🛠️ Approach
The solution uses Excel formulas:

1. **Lookup Order Priority**
   ```excel
   =VLOOKUP(A2, Orders!A:B, 2, FALSE)
